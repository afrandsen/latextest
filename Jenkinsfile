pipeline {
   agent none
   stages {
      stage('Build1') {
         agent {
            docker {
               image 'python:3.11.0-alpine'
            }
         }
         steps {
             sh 'python3 figure.py'
         }
      }
   }
}