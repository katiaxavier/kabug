pipeline {
    agent any
    
    stages {
        stage('Build'){
            steps{
                echo 'Building or Resolve Dependencies!'
                sh 'bundle install'
            }
        }
        stage('Test'){
            steps{
                echo 'Runing regression tests'
            }
        }
        stage('UAT'){
            steps{
                echo 'Wait for User acceptance'
                input(message: 'Go to production?', ok: 'Yes' )
            }
        }
        stage('Prod'){
            steps{
                echo 'WebApp is Ready!'
            }
        }
    }
}