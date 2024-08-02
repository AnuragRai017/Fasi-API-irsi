

# Iris Species Prediction API

This is a simple API built with FastAPI that allows you to predict the species of an iris flower based on its sepal and petal measurements. The prediction is made using a Logistic Regression model trained on the Iris dataset from scikit-learn.

## Features

- **Predict Iris Species:** Provide sepal and petal measurements to predict the species of the iris flower.
- **FastAPI:** A modern, fast (high-performance), web framework for building APIs with Python 3.6+.
- **Scikit-learn:** Used for training the Logistic Regression model.

## Endpoints

### Root (`/`)

- **Method:** GET
- **Description:** Returns a description of the API and how to use it.

### Predict (`/predict/`)

- **Method:** POST
- **Description:** Predicts the species of the iris flower based on the provided sepal and petal measurements.
- **Request Body:**
  - `sepal_length`: *float* - Sepal length of the iris flower.
  - `sepal_width`: *float* - Sepal width of the iris flower.
  - `petal_length`: *float* - Petal length of the iris flower.
  - `petal_width`: *float* - Petal width of the iris flower.
- **Response:**
  - `species`: *string* - The predicted species of the iris flower.

## Example Request

To predict the species of an iris flower, you can use the following example:

### Request

```bash
POST /predict/
Content-Type: application/json

{
  "sepal_length": 5.1,
  "sepal_width": 3.5,
  "petal_length": 1.4,
  "petal_width": 0.2
}
```

### Response

```json
{
  "species": "setosa"
}
```

## Installation

### Prerequisites

- Python 3.6+
- Pip (Python package installer)

### Steps

1. **Clone the Repository:**

   ```bash
   git clone <your-repo-url>
   cd <your-repo-directory>
   ```

2. **Create a Virtual Environment:**

   ```bash
   python -m venv env
   ```

3. **Activate the Virtual Environment:**

   - On Windows:
     ```bash
     env\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source env/bin/activate
     ```

4. **Install the Required Packages:**

   ```bash
   pip install fastapi scikit-learn uvicorn pydantic
   ```

5. **Run the FastAPI App:**

   ```bash
   uvicorn main:app --reload
   ```

6. **Access the Application:**

   Open your web browser and go to `http://127.0.0.1:8000/` to see the root endpoint or go to `http://127.0.0.1:8000/docs` to access the interactive API documentation.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or feedback, feel free to reach out to me at anuragrai0714@gmail.com.

