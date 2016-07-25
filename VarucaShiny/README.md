
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="880" alt="Visit QuantNet">](http://quantlet.de/index.php?p=info)

## [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/) **VarucaShiny** [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/d3/ia)

```yaml

Name of Quantlet : VarucaShiny

Published in : 'Visualization of cross tabulation by the Association rules by using the
Correspondence analysis: Compstat2016'

Description : 'Shiny application of the Visualization of cross tabulation of questionnaire by media
layers based on gender and age. The visualization used association rules and the biplot of
correspondence analysis.'

Keywords : questionnaire, association rules, correspondence analysi

Author[New] : Sanetoshi Yamada and Yoshiro Yamamoto

Submitted : 2016-07-22, Yoshiro Yamamoto

Output : Plot of the association rule plot using the biplot of the correspondence analysis.

```

![Picture1](varucaShiny.png)


### R Code:
```r
require(devtools)
require(shiny)
runApp(paste(getwd(),"/ShinyApp/varucashiny",sep = ""))

```
