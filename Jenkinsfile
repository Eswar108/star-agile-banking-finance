pipeline{
    agent any
    stages{
        stage('checkout the code from github'){
            steps{
                 git url: 'https://github.com/akshu20791/DevOpsClassCodes/'
                 echo 'github url checkout'
            }
        }
        stage('codecompile with Eswar'){
            steps{
                echo 'starting compiling'
                sh 'mvn compile'
            }
        }
        stage('codetesting with Eswar'){
            steps{
                sh 'mvn test'
            }
        }
        stage('qa with Eswar'){
            steps{
                sh 'mvn checkstyle:checkstyle'
            }
        }
        stage('package with Eswar'){
            steps{
                sh 'mvn package'
            }
        }
      stage('run docker file'){
          steps{
              sh 'docker build -t myimg .
          }
      }
    }
}
