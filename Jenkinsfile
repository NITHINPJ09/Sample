pipeline {
    agent any

    stages {
        
        stage('Version') {
            when {
                branch 'feature'
            }
            steps {
                sh 'java --version'
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
