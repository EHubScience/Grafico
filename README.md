# Grafico
Gráfico para Definição de Principais Variáveis para Modelo de Machine Learning com RStudio
install.packages("ggplot2")
library(ggplot2)
ggplot(rankImportance,
       aes(x=reorder(variables,Importance),
           y=Importance,
           fill=Importance)) +
  geom_bar(stat='identity') +
  geom_text(aes(x=variables,y=0.5,label=Rank),
            hjust=0,
            vjust=0.55,
            size=4,
            colour='red')+
  labs(x='Variables')+
  coord_flip()
