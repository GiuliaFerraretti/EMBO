# EMBO
#Matteo Fumagalli 11/06
#Predict the allele frequency after the next 100 generation under the Wright Fisher model   
N=50
fA=0.6
rbinom(100,2*N, 0.6)

rep_100=rbinom(100,2*N, 0.6)
mean(rep_100)

rep_100_div=rep_100/100
mean(rep_100_div)

rep_100_0.4=rbinom(100,100, 0.4)
rep_100_0.4_div=rep_100_0.4/100
mean(rep_100_0.4_div)



freq = c(0.7,0.2,0.3)
#for k freq {
#  rbinom (100,2*N, freq)/2*N
#}

#Predict the allele frequency after the very first next generation under the Wright Fisher model

rep_single=rbinom(1,100, 0.4) / 100
rep_single_2=rbinom(1,100, 0.4) /100
rep_single_3=rbinom(1,100, 0.4) /100
rep_single_4=rbinom(1,100, 0.4) /100
mean(rep_single + rep_single_2)


total= rep_single + rep_single_2 + rep_single_3 + rep_single_4
mean= total / 4

x=1:1000
y=rbinom (1000, 30, 0.3 ) / 30
y_2=rbinom (1000, 60, 0.3 ) / 60
plot(x,y,type = "l" , ylim = c(0,0.7))
plot(x,y_2,type = "l" , ylim = c(0,0.7))
