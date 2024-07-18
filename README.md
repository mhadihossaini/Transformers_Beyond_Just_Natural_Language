### Semantic Similarity with Transformers

This project constructs a latent space for scientific papers in the DIT publication database using transformer models. By analyzing the abstracts and identifying semantic similarities, the project recommends potential author collaborations based on the Euclidean distances between paper embeddings.

#### Project Structure
- person.json: JSON file containing the abstracts and authors of the scientific papers.
- Transformers_Beyond_Just_Natural_Language.ipynb: Jupyter notebook containing the code for processing the abstracts, constructing embeddings, and finding similar authors.

#### Methodology

- **Data Preprocessing:**
  - Load the abstracts and author data from the JSON file.
  - Clean and prepare the text data for embedding generation.

- **Embedding Generation:**
  - Use a pre-trained transformer model from Hugging Face to convert the abstracts into embeddings.
  - Each abstract is represented as a vector in the latent space.

- **Distance Calculation:**
  - Compute the Euclidean distances between each pair of paper embeddings.
  - Aggregate distances for authors based on their co-authored papers.

- **Author Recommendations:**
  - For each author, find the 5 closest authors who are not co-authors.
  - Output the recommendations for potential collaborations.
