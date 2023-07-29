pipeline {
    agent { label 'WS' }
    stages {
        stage('Lint Checks') {                                          // Start of the stages
            steps {
                sh "echo Installing JSLint"
                sh "npm i jslint"
                sh "ls -lrt node_modules/jslint/bin"
                sh "/home/centos/node_modules/jslint/bin/jslint.js server.js || true"
            }
        }                                                                
        stage('Code Compile') {
            steps {
                sh "npm install"
            }
        }
    }                                                                   // End of the stages
}