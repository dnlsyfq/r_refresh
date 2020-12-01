# 
# packt <- c('readr','dplyr')
# for(packages in packt){
#   install.packages(packages)
# }


library(dplyr)
library(readr)

artists <- read.csv('artists.csv')
# print(artists)

head(artists)

summary(artists)

artists %>% 
    select(-country,-year_founded,-albums) %>% 
    filter(spotify_monthly_listeners > 20000000, genre != 'Hip Hop') %>% 
    arrange(desc(youtube_subscribers))