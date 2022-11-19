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
             sh 'pip3 install matplotlib'
             sh 'pip3 install numpy'
             sh 'pip3 install tikzplotlib'
             sh 'python3 figure.py'
         }
      }
   }
}