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
             sh 'pip3 install --target ${env.WORKSPACE} matplotlib'
             sh 'pip3 install --target ${env.WORKSPACE} numpy'
             sh 'pip3 install --target ${env.WORKSPACE} tikzplotlib'
             sh 'python3 figure.py'
         }
      }
   }
}