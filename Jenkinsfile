@Library('roboshop-shared-library') _                     // Always at the start of the line

pipeline {
    agent { label 'WS' }
    stages {
        stage('Lint Checks') {                                          // Start of the stages
            steps {
                script {
                    nodejs.lintChecks()
                }
            }
        }                                                                
        stage('Code Compile') {
            steps {
                sh "npm install"
            }
        }
    }                                                                   // End of the stages
}