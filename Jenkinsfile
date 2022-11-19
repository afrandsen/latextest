pipeline {
   agent none
   stages {
      stage('Build1') {
         agent {
            docker {
               image 'python:3.10.0-alpine'
            }
         }
         steps {
                  sh 'python -m pip install matplotlib'
                  sh 'python -m pip install numpy'
                  sh 'python -m pip install tikzplotlib'
                  sh 'python3 figure.py'
         }
      }
   }
}