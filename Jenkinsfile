pipeline{
    agent any
    stages{
        stage ('Repo'){
            steps{
                git branch: 'main', url: 'https://github.com/jacodetunde/React-Django-WebApp.git'
            }
        }
        stage('Testing'){
            steps{
                echo "Testing"
            }
        }
        stage('Build'){
            steps{
                script{
                    sh "docker build — no-cache -t react_django_demo_app ."
                }
            }
        }
        stage('Run'){
            steps{
                script{
                    sh "docker run -p 8080:8001 -d react_django_demo_app"
                }
            }
        }
    }
}