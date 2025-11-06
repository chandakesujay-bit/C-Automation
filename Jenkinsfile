pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning GitHub repository...'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling the C program...'
                sh 'gcc -o app example.c'
            }
        }

        stage('Run') {
            steps {
                echo 'Running the compiled program...'
                sh './app'
            }
        }
    }

    post {
        success {
            echo '✅ Build and run completed successfully!'
        }
        failure {
            echo '❌ Build or run failed!'
        }
    }
}
