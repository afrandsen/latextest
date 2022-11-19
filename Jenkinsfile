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
             withEnv(["HOME=${env.WORKSPACE}"]) {
                  sh 'pip install matplotlib'
                  sh 'pip install numpy'
                  sh 'pip install tikzplotlib'
                  sh 'python3 figure.py'
             }
         }
      }
   }
}