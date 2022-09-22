pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
    }

    stages 
    {
        stage('Build') 
        {
            steps {
                echo 'Build App'
            }
        }
        stage('Test') 
        {
            steps {
                echo 'Test App'
            }
        }
        stage('Maven') 
        {
            steps {
                sh 'clean install'
            }
        }
    }
    post
    {
        always
        {
         emailext body: 'Summary', subject: 'Pipeline Status', to: 'maha1982002@gmail.com'   
        }
    
        }
    }
