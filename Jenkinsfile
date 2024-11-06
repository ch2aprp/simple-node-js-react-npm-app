pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
                script {
                    powersheel 
                    ''' 
                    Write-Output "Hello World!"
                    $date = Get-Date
                    Write-Output "Current Date and time : $date"
                    '''
                }
                script {
                    powersheel '''./scripts/script-hello.ps1'''
                }
            }
        }
    }
}