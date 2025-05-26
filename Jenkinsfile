pipeline {
    agent any

    tools {
        maven 'Maven-3.8.6' // Must match the name from step 1
    }

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/your-username/your-repo.git' // replace with your repo
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package' // use 'bat' if on Windows: bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test' // run unit tests
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...' // replace with actual deploy logic
            }
        }
    }

    post {
        success {
            echo '✅ Build Successful!'
        }
        failure {
            echo '❌ Build Failed!'
        }
    }
}
