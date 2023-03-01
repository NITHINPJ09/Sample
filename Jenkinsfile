pipeline {
    agent any

    stages {
        
        stage('Version') {
             when {
                 expression {
                    return env.BRANCH_NAME == 'master';
                 }             
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
