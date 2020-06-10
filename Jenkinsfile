pipeline {
    agent {
        docker {
            image 'katiaxavier/rubywd'
        }
    }
    
    stages {
        stage('Build'){
            steps{
                echo 'Building or Resolve Dependencies!'
                sh 'rm -f Gemfile.lock'
                sh 'bundle install'
            }
        }
        stage('Test'){
            steps{
                echo 'Runing regression tests'
                sh 'bundle exec cucumber -p ci'
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