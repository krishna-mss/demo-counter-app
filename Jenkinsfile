pipeline{
    agent any
    stages{
        stage('git checkout'){
            steps{
                git 'https://github.com/krishna-mss/demo-counter-app.git'
            }
        }
        stage('build'){
            steps{
                script{
                    sh 'mvn clean install'
                }
            }
        }
    }
}