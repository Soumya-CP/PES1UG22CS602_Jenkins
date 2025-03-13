pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                    cd $WORKSPACE  # Go to Jenkins workspace
                    pwd
                    ls -la  # Debugging: Check files
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
