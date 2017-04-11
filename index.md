
################ Data Input###############
xx=sort(c(12,44,34,14.01,9,19,156,23.01,13,11,47,26,14,33,15,61.99,5,8,0,154,146.01), decreasing=F)
yy=sort(c(37,39,30,7,13.01,139,45,25,16.01,146,94,16,23,1,290,169,62,145,36,20,12.99), decreasing=F)

######### Exact Mann-Whitney-Wilcoxon Test #########################
wilcox.test(yy,xx, exact=T, alternative = "g")


##Asymptotic Mann-Whitney-Wilcoxon test with  no continuity correction #######################
wilcox.test(yy,xx,exact=F, alternative = "g", correct = F)


####### Asymptotic Mann-Whitney-Wilcoxon test with continuity correction ###########################
wilcox.test(yy,xx,exact=F, alternative = "g", correct = T)
