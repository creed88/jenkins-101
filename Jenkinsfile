pipeline {
    agent {
        label 'docker-agent'  // This label must match what you set under Docker Cloud template
    }
    stages {
        stage('Preparation') {
            steps {
                echo 'Running on Docker agent using jenkins/inbound-agent...'
                sh 'whoami'
                sh 'hostname'
            }
        }

        stage('Checkout Code') {
            steps {
                git 'https://github.com/creed88/jenkins-101.git' // replace with your actual repo
            }
        }

        stage('Build') {
            steps {
                echo 'Simulating build...'
                sh 'echo "Build completed2"'
            }
        }

        // stage('Test') {
        //     steps {
        //         echo 'Running tests...'
        //         sh 'echo "All tests passed!"'
        //     }
        // }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo "Deploy complete!"'
            }
        }
    }
}
