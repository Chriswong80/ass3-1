# R code to perform ANOVA and generate Part Resistance boxplot for Machine 1 by Temperature
data_machine1 <- X037 %>% filter(Machine == 1)
anova_result <- aov(PartResistance ~ factor(Temperature), data = data_machine1)
summary(anova_result)
data_machine1$Temperature <- as.factor(data_machine1$Temperature)
okabe_ito_colors <- c("#0072B2", "#D55E00", "#009E73", "#CC79A7", "#F0E442", "#56B4E9", "#E69F00", "#FFFFFF")
p <- ggplot(data_machine1, aes(x = Temperature, y = PartResistance, fill = Temperature)) +
  geom_boxplot() +
  scale_fill_manual(values = okabe_ito_colors) +
  labs(title = "Part Resistance by Temperature (Machine 1)",
       x = "Temperature",
       y = "Part Resistance") +
  theme_minimal() +
  theme(axis.title.x = element_text(size = 18),
        axis.title.y = element_text(size = 18),
        axis.text.x = element_text(size = 14, angle = 0, hjust = 0.5),
        axis.text.y = element_text(size = 14),
        legend.position = "none",
        plot.background = element_rect(fill = "white", colour = NA))
pg <- ggplotly(p)
htmlwidgets::saveWidget(pg, "media/plots/machine1_resistance_boxplot_temperature_anova.html", selfcontained = TRUE)
