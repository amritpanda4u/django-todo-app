pipeline {
    agent any
    
    stages {
        stage('Code'){
            steps {
                git credentialsId: 'github', url: 'git@github.com:amritpanda4u/django-todo-app.git', branch: 'main'
            }
           }
        stage('Build'){
            steps {
                sh 'docker-compose down'
                sh 'docker-compose up -d'
            }
            
        }
        stage('Test'){
            steps {
                echo 'Testing ...'
            }
            
        }
        stage('Deploy'){
            steps {
                echo 'Deploying'
            }
            
        }
    }
}
