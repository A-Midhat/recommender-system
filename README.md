This project implements two models for building a recommender system:

1. **Biases-Only Model**: A simple model that predicts ratings based on user and movie biases.
2. **Biases + Latents Model**: An improved model that adds user and movie latent factors to capture hidden preferences and attributes.

## Models

### Biases-Only Model
- Predicts ratings using:
  
  $\hat{r}_{um} = b_u + b_m$
  
- **How it works**:
  - **User bias** ($b_u$): Captures how much a user tends to rate higher or lower than average.
  - **Movie bias** ($b_m$): Captures how popular a movie is overall.
- This model is a simple baseline for recommendation tasks.

### Biases + Latents Model
- Extends the Biases-Only Model by adding latent factors:
  
  $\hat{r}_{um} = b_u + b_m + u_u^T v_m$
  
- **How it works**:
  - Latent factors ($u_u$, $v_m$): Represent hidden features like a user’s preferences or a movie’s genres.
  - The dot product ($u_u^T v_m$) helps capture complex interactions between users and movies.
- This model provides better predictions by modeling deeper relationships in the data.

