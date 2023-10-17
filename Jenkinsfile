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
        stage('Clean') {
            steps {
                sh "mvn clean"
            }
        }
        // stage('Validate') {
        //     steps {
        //         sh "mvn validate"
        //     }
        // }
        // stage('Compile') {
        //     steps {
        //         sh "mvn compile"
        //     }
        // }
        
        // stage('Package') {
        //     steps {
        //         sh "mvn clean package"
                
        //          }
        // }     
    }
}
