pipeline {
    agent {
        node {
            label 'docker_agent_python'
        }
    }
    triggers{
        pollSCM '*/1 * * * *'
    }
    stages{
        stage('Build') {
            steps {
                echo "Building..."
                sh '''
                    echo "Building my first pipeline through Jenkinsfile"
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing..."
                sh '''
                    echo "Testing my pipeline"
                    python3 test_jenkins.py
                    which python3
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo "Delivering..."
                sh '''
                    echo "Delivering the application"
                '''
            }
        }
    }
}