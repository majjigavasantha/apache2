pipeline {
    
    agent { label 'master' }


    tools {
    jdk 'Java8'
    maven 'Maven3.3.9'

  }

    stages {
        
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/chinni4321/apache2.git'

            }

        }
        stage('aws') {
            steps {
                // Get some code from a GitHub repository
                sh  '''
                  cd apache2
                  aws s3 cp * s3://prashanth41234154 
                  '''

            }
        }
      }
     }
