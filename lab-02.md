Lab 02 - Plastic waste
================
Ève Chartrand
20-09-25

## Chargement des packages et des données

View(plastic_waste)

``` r
library(tidyverse) 
```

``` r
plastic_waste <- read_csv("data/plastic-waste.csv")
```

Commençons par filtrer les données pour retirer le point représenté par
Trinité et Tobago (TTO) qui est un outlier.

``` r
plastic_waste <- plastic_waste %>%
  filter(plastic_waste_per_cap < 3.5)
```

## Exercices

ggplot(data = plastic_waste, aes(x = plastic_waste_per_cap)) +
geom_histogram(binwidth = 0.2)

plastic_waste %\>% filter(plastic_waste_per_cap \> 3.5)

plastic_waste \<- plastic_waste %\>% filter(plastic_waste_per_cap \<
3.5)

### Exercise 1

``` r
ggplot(data = plastic_waste, aes(x = plastic_waste_per_cap)) +
  geom_histogram() +
  facet_grid(. ~ continent)
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](lab-02_files/figure-gfm/plastic-waste-continent-1.png)<!-- -->

### Exercise 2

``` r
ggplot(plastic_waste, aes(x = plastic_waste_per_cap, colour = continent, fill = continent)) +
    geom_density(alpha = 0.4)
```

![](lab-02_files/figure-gfm/plastic-waste-density-1.png)<!-- -->

Le réglage de la couleur se fait dans aes puisque ces modifications
dépendent des données. Le réglage de alpha se fait dans la section geom
puisque cette propriétée ne dépend pas des variables du graphique, mais
plutôt de l’allure du graphique.

### Exercise 3

Boxplot:

``` r
# insert code here
```

Violin plot:

``` r
# insert code here
```

Réponse à la question…

### Exercise 4

``` r
# insert code here
```

Réponse à la question…

### Exercise 5

``` r
# insert code here
```

``` r
# insert code here
```

Réponse à la question…

## Conclusion

Recréez la visualisation:

``` r
# insert code here
```
