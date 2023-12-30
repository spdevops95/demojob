pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

         {
          
       stage('Build') {
            steps {
                // Your build commands go here
                sh 'echo "Building..."'
                sh 'mvn clean install'  // Replace with your actual build command
            }
                
            }
        }

        stage('Test') {
            steps {
                 // Your test commands go here
                sh 'echo "Running tests..."'
                sh 'mvn test'  // Replace with your actual test command
            }
        }

        stage('Deploy') {
            steps {
                sh './deploy.sh'
            }
        }
    }
}

