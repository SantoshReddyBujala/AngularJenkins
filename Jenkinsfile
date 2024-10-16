pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('node:16-alpine').inside { 
                        sh 'npm install -g @angular/cli'
                        sh 'npm install'
                        sh 'ng build --prod' 
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    docker.image('node:16-alpine').inside { 
                        sh 'ng test --watch=false --browsers=ChromeHeadless' 
                    }
                }
            }
        }
    }
}
