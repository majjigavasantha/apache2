pipeline {
    
    agent any


    tools {
    jdk 'java8'
    maven 'maven'

  }

    stages {
        
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repository
               git branch: 'main',
               url: 'https://github.com/majjigavasantha/apache2.git'
            }

        }
        stage('aws') {
            steps {
                // Get some code from a GitHub repository
                sh  '''
                  cd $WORKSPACE
                  aws s3 sync . s3://demo-15544
                  '''

            }
        }
      }
     }
