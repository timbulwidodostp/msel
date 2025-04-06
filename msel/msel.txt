# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Multivariate and multinomial sample selection and endogenous switching models with multiple outcomes Use msel (switchSelection) With (In) R Software
install.packages("switchSelection")
library("switchSelection")
msel = read.csv("https://raw.githubusercontent.com/timbulwidodostp/msel/main/msel/msel.csv",sep = ";")
# Estimation Multivariate and multinomial sample selection and endogenous switching models with multiple outcomes Use msel (switchSelection) With (In) R Software
msel$educ                     <- NA
msel$educ[msel$basic == 1]    <- 0
msel$educ[msel$bachelor == 1] <- 1
msel$educ[msel$master == 1]   <- 2
f_work <- work ~ age + I(age ^ 2) + bachelor + master + health + slwage + nchild
msel_1 <- msel(f_work, data = msel)
summary(msel_1)
f_educ <- educ ~ age + I(age ^ 2) + sbachelor + smaster
msel_2 <- msel(f_educ, data = msel)
summary(msel_2)
# Multivariate and multinomial sample selection and endogenous switching models with multiple outcomes Use msel (switchSelection) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished