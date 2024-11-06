pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
                script {
                    powershell 
                    ''' 
                    Write-Output "Hello World!"
                    $date = Get-Date
                    Write-Output "Current Date and time : $date"
                    '''
                }
                script {
                    powershell '''./scripts/script-hello.ps1'''
                }
            }
        }
    }
}