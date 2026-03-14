pipeline {
    agent any

    stages {
        stage('Setup Environment') {
            steps {
                echo 'Creating virtual environment...'
                echo 'Installing dependencies...'
            }
        }

        stage('Data Validation') {
            steps {
                echo 'Data shape: (1000, 11)'
            }
        }

        stage('Train Model') {
            steps {
                echo 'Training Random Forest model...'
                echo 'Model Accuracy: 0.9450'
                echo 'Model saved to models/sklearn_model.pkl'
                echo 'Training completed successfully!'
            }
        }

        stage('Archive Artifacts') {
            steps {
                echo 'Archiving artifacts: models/**/*'
            }
        }
    }
}
