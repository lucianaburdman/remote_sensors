# Set seed to ensure reproducibility
set.seed(123)

# Generate random data
data <- matrix(rnorm(100), nrow = 10, ncol = 10)

# Create a map using the ggplot2 library
library(ggplot2)

ggplot() + 
  geom_tile(data = data, aes(x = 1:nrow(data), y = 1:ncol(data), fill = value)) +
  scale_fill_gradient(low = "blue", high = "red")
