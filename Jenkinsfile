pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
            steps {
                script {
                    powersheel 
                    ''' 
                    Write-Output "Hello World!"
                    $date = Get-Date
                    Write-Output "Current Date and time : $date"
                    '''
                }
            }
            steps {
                script {
                    powersheel '''./scripts/script-hello.ps1'''
                }
            }
        }
    }
}