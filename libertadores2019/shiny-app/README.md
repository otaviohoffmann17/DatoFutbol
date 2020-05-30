library(dplyr)
# Ajusta modelo con datos antiguos (2011-2019)
old_data <- read.csv("data_liberta_2011_19.csv", stringsAsFactors=F,
                      encoding="utf8")
fit <- glm(factor(clas_factor) ~ Value_centered, old_data,
           family='binomial')
# Nuevos datos
new_data <- read.csv("grupos_2020.csv", stringsAsFactors=F,
                     encoding="utf8")
# Centra valores $ respecto a grupos
mean_values <- new_data %>% group_by(Year, Group) %>% 
               summarise(mean_value=mean(Value))
new_data <- new_data %>% inner_join(mean_values, by="Group") %>%  
            mutate(Value_centered = Value - mean_value)
# Usa modelo para estimar probs. independientes de datos 2020
new <- data.frame(Value_centered = new_data$Value_centered)
p <- predict(fit, newdata = new, type="response")
new_data <- new_data %>% mutate(P_ind=p)
# Normaliza probabilidades por grupo y rankea de mayor a menor
sum_values <- new_data %>% group_by(Group) %>%
              summarise(sum_p=sum(P_ind))
new_data <- new_data %>% inner_join(sum_values, by="Group") %>%
            mutate(P_norm = round(P_ind/sum_p*100, 1)) %>%
            select(Group, Club, Value, Value_centered, P_ind,
                   P_norm) %>%
            arrange(Group, desc(P_norm))
