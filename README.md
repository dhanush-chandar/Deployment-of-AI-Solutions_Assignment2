# Deployment-of-AI-Solutions_Assignment2

## Overview
This project demonstrates a simple machine learning application using Flask and Docker. The application uses a Decision Tree Classifier to predict the species of an iris flower based on its sepal and petal dimensions.

## Project Structure
The project contains the following files:
- `Dockerfile`: Instructions to build the Docker image for the application.
- `requirements.txt`: Lists the Python packages required for the application.
- `train_model.py`: Script to train the Decision Tree model using the Iris dataset.
- `app.py`: Flask application to handle predictions.
- `model.pkl`: The trained model saved for making predictions.

## Instructions to Build and Run the Docker Container

1. **Clone the repository**:
   ```bash
   git clone https://github.com/dhanush-chandar/Deployment-of-AI-Solutions_Assignment2.git
   cd Deployment-of-AI-Solutions_Assignment2
   
2. Build the Docker image:
sudo docker build -t ml-app .

3. Run the Docker container:
sudo docker run -p 4000:80 ml-app

4. Access the Application: Open your browser and navigate to http://localhost:4000 to see the running application.

## Testing the ML Endpoint

You can test the /predict endpoint using curl or Postman by sending a POST request with JSON data. For example:
curl -X POST http://localhost:4000/predict -H "Content-Type: application/json" -d '{"input": [5.1, 3.5, 1.4, 0.2]}'

You should receive a JSON response containing the predicted species:
{"prediction": 0}

## Technologies Used
Python 3.9
Flask
Scikit-learn
Docker

## Acknowledgements
This project utilizes the Iris dataset from the Scikit-learn library for training the machine learning model.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
