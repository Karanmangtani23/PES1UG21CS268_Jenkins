pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo "Build"'
                build 'PES1UG21CS268-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "Test"'
                sh './output'

            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "Deployment"' 
                sh 'echo "🚒"'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
