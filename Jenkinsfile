pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:22.17.0-alpine3.22'
                    reuseNode true
                }
            }
            steps {
                sh'''
                    ls -la
                    node --version
                    npm --version
                    npm install
                    npm run build
                    ls -la
                '''
            }
    }
        stage('Test') {
                steps{
                    sh 'echo "test stage"'
                }
            }
}