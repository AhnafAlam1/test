# test

install.packages("tidyverse")
install.packages("janitor")

library(tidyverse)
library(janitor)

simulated_data <-
  tibble(
    # use 1 through 151 to represent each division
    "Division" = 1:151,
    # randomly pick an option, with replacement, 151 times
    "Party"= sample(
      x = c("Liberal","Labor", "National", "Green", "Other"),
      size = 151,
      replace = TRUE
    )
  )
simulated_data