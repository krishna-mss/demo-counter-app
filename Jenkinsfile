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
        stage('static code analysis'){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-app') {
                        sh "mvn clean package sonar:sonar"
                    }
                }
            }
        }
    }
}