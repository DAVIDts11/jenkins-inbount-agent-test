pipeline {
    // agent { label 'inb-agent-test' }
    agent { label 'dind-agent' }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }

        stage('Verify Python') {
            steps {
                sh '''
                python3 --version
                pip3 --version
                '''
            }
        }
        
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run') {
            steps {
                sh 'python3 main.py'
            }
        }
    
    }
}
