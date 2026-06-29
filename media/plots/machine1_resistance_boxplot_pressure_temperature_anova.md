# R code to perform ANOVA and generate Part Resistance boxplot for Machine 1 by Pressure and Temperature
data_machine1 <- X037 %>% filter(Machine == 1)
data_machine1$Pressure <- as.factor(data_machine1$Pressure)
data_machine1$Temperature <- as.factor(data_machine1$Temperature)
anova_result_pt <- aov(PartResistance ~ Pressure * Temperature, data = data_machine1)
summary(anova_result_pt)
okabe_ito_colors <- c("#0072B2", "#D55E00", "#009E73", "#CC79A7", "#F0E442", "#56B4E9", "#E69F00", "#FFFFFF")
p_pt <- ggplot(data_machine1, aes(x = interaction(Pressure, Temperature), y = PartResistance, fill = interaction(Pressure, Temperature))) +
  geom_boxplot() +
  scale_fill_manual(values = okabe_ito_colors[1:length(unique(interaction(data_machine1$Pressure, data_machine1$Temperature)))]) +
  labs(title = "Part Resistance by Pressure and Temperature (Machine 1)",
       x = "Pressure:Temperature Interaction",
       y = "Part Resistance") +
  theme_minimal() +
  theme(axis.title.x = element_text(size = 18),
        axis.title.y = element_text(size = 18),
        axis.text.x = element_text(size = 14, angle = 45, hjust = 1),
        axis.text.y = element_text(size = 14),
        legend.position = "none",
        plot.background = element_rect(fill = "white", colour = NA))
pg_pt <- ggplotly(p_pt)
htmlwidgets::saveWidget(pg_pt, "media/plots/machine1_resistance_boxplot_pressure_temperature_anova.html", selfcontained = TRUE)
