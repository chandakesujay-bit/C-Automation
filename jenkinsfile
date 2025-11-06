pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps { git 'https://github.com/<your-username>/c-automation-demo.git'i  }
        }
        stage('Build') {
            steps { sh 'gcc -o app main.c' }
        }
        stage('Run') {
            steps { sh './app' }
        }
    }
    post {
        success { echo '✅ C build completed successfully!' }
        failure { echo '❌ Build failed!' }
    }
}
~

