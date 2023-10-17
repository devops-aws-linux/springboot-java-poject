pipeline {   
    agent any 
    tools{
        jdk 'java11'
        maven 'maven3'
    }

    stages {
        stage('Git checkout') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/devops-aws-linux/springboot-java-poject.git'
            }
        }
        stage('validate'){
            steps{
                sh 'mvn validate'
            }
        } 
        stage('compile'){
            steps{
                sh 'mvn compile'
            }
        }   
    }
}
