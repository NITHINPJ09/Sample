pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/NITHINPJ09/Sample.git'
            }
        }
        stage('Compile') {
            steps {
                sh 'javac Welcome.java'
            }
        }
        
        stage('Run') {
            steps {
                sh 'java Welcome'
            }
        }
    }
}
