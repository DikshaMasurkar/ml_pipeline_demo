pipeline {
    agent any

    parameters {
        choice(name: 'FRAMEWORK', choices: ['sklearn','tensorflow','pytorch'], description: 'Select ML Framework')
    }

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/DikshaMasurkar/ml_pipeline_demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Train Model') {
            steps {
                sh "python train.py --framework ${FRAMEWORK}"
            }
        }

        stage('Save Model') {
            steps {
                sh 'mkdir -p models'
            }
        }

    }
}
