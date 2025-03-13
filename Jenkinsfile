pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                    cd /path/to/your/main/directory
                    g++ -o PES1UG22CS602-1 PES1UG22CS602_Soumya-C-P.cpp
                    '''
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS602-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying application...'
                    // Add actual deployment commands (e.g., SCP, Docker, Kubernetes, etc.)
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
