pipeline {
    agent any
    stages {
                
        stage('Build and Run Tests') {
            steps {
                // Build your application and run tests
                // Redirect your application's logs to a file (e.g., log.txt)
                sh 'javac Welcome.java > log.txt'
                sh 'echo "Testing--------------------------------------------------"'
                sh 'cat log.txt'
            }
        }
        stage('Parse Log for Errors') {
            steps {
                script {
                    // Use the Log Parser Plugin to highlight errors
                    def logParser = logParser(pattern: 'ERROR: (.*)', status: 'ERROR')
                    def logFile = readFile('log.txt')
                    def parsedLog = logParser.parseLog(logFile)

                    // Output the parsed log to the console
                    echo(parsedLog)
                }
            }
        }
    }
}
