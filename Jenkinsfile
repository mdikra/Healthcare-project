pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/mdikra/Healthcare-project.git', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t danishdockerhub/staragile-project-health:v1 .'
                    sh 'docker images'
                }
            }
        }
         
