pipeline{
    agent any
    stages{
        stage{
            steps{
                git branch: 'main', url: 'https://github.com/jacodetunde/React-Django-WebApp.git'
            }
        }
        stage{
            steps{
                echo "Testing"
            }
        }
        stage{
            steps{
                script{
                    sh "docker build — no-cache -t react_django_demo_app ."
                }
            }
        }
        stage{
            steps{
                script{
                    sh "docker run -p 8080:8001 -d react_django_demo_app"
                }
            }
        }
    }
}