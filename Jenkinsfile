pipeline {
    agent any
    stages {
                
        stage('Compile') {
            steps {
                sh 'javac Welcome.java'
            }
        }
        
        stage('Run') {
            steps {
                sh 'java Welcome'
                sh 'ls -a'
            }
        }
        
    }
}
