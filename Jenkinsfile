pipeline {
    tools{
        maven 'mvn'
        jdk 'jdk8'
    }
    agent any

    stages {
        stage('checkout') {
            steps {
                git 'https://github.com/Yash4523/DevOpsClassCodes.git'
            }
        }
            stage('project'){
                steps{
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('code coverage'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
