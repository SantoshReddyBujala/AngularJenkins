pipeline { 
    agent any
    stages {
        stage("build") {
            steps{
                 bat  "npm install"
                 bat "npm run ng build --prod"
            }
        }
    }
}
