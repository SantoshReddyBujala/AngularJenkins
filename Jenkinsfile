pipeline { 
    agent any
    stages {
        stage("checkout") {
            steps{
                bat "dir"
                git branch: 'main', url: 'https://github.com/SantoshReddyBujala/AngularJenkins.git'
                bat "dir"
            }
        }
        stage("build") {
            steps{
                 bat  "npm install"
                 bat "npm run ng build --prod"
            }
        }
    }
}