pipeline { 
    agent any
    stages {
      stage("node") {
            steps{
                 bat "node --version"
            }
        }
      stage("java") {
            steps{
                 bat "java --version"
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
