
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="880" alt="Visit QuantNet">](http://quantlet.de/index.php?p=info)

## [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/) **Varuca** [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/d3/ia)

```yaml

Name of Quantlet : Varuca

Published in : 'Visualization of cross tabulation by the Association rules by using the
Correspondence analysis: Compstat2016'

Description : 'Visualization of cross tabulation of questionnaire by media layers based on gender
and age. The visualization used association rules and the biplot of correspondence analysis.'

Keywords : questionnaire, association rules, correspondence analysi

Author[New] : Sanetoshi Yamada and Yoshiro Yamamoto

Submitted : 2016-07-18, Yoshiro Yamamoto

Output : Plot of the association rule plot using the biplot of the correspondence analysis.

```

![Picture1](Rplot.png)


### R Code:
```r
#install.packages("arules")
#install.packages("arulesViz")
#install.packages("manipulate")

library("arules")
library("arulesViz")
library("MASS")

#AD <- read.csv("questionnaire.csv",row.names=1)
#ML <- read.csv("monitor.csv",row.names=1)
attach(ML)
#QD <- read.csv("Content.csv",row.names=1)
MC="Media"

source("AP.R")
AP(Q="Q15",Cex=1,As=25,Ms=50,Supp=0.01,Conf=0.1,Lift=1.3,l=2,Lhs="M")

library("manipulate")
manipulate(AP(Q,Cex,As,Ms,supp,conf,lift,2,Lhs),
           Q=picker(as.list(row.names(QD[QD[,1]=="MA",])),initial="Q15"),
           Lhs=picker("M","A"),
           supp=slider(0,0.1,initial=0.01,step=0.001),
           conf=slider(0,1,initial=0.1,step=0.01),
           lift=slider(0.1,2,initial=1.3,step=0.1),
           Cex=slider(0.1,2,1),
           As=slider(0,100,25),
           Ms=slider(0,100,50)
           )

```
