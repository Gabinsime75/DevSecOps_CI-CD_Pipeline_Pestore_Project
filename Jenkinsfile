pipeline{
    agent any
    tools {
        jdk 'jdk17'
        maven 'maven3'

    }
    environment {
        SCANNER_HOME=tool 'sonar-scanner'
    }


    stages{
        stage ('clean Workspace'){
            steps{
                cleanWs()
            }
        }
        stage ('checkout scm') {
            steps {
                git branch: 'main', url: 'https://github.com/Gabinsime75/DevSecOps_CI-CD_Pipeline_Pestore_Project.git'
            }
        }
        stage ('maven compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage ('maven Test') {
            steps {
                sh 'mvn test'
            }
        }


   }
}
