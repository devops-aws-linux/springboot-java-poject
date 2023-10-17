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
        stage('test'){
            steps{
                sh 'mvn test'
            }
        } 
        stage('package'){
            steps{
                sh 'mvn package'
            }
        } 
        stage('install'){
            steps{
                sh 'mvn install'
            }
        } 
        stage('clean'){
            steps{
                sh 'mvn clean package'
            }
        }   
    }
}
