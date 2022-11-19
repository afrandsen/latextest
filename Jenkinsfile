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
               withEnv(["HOME=${env.WORKSPACE}"]) {
                  sh 'pip3 install matplotlib --user'
                  sh 'pip3 install numpy --user'
                  sh 'pip3 install tikzplotlib --user'
                  sh 'python3 figure.py'
               }
         }
      }
   }
}