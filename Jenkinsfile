pipeline {
   agent none
   stages {
      stage('Build1') {
         agent {
            docker {
               image 'python:3.10.7-alpine'
            }
         }
         steps {
             sh 'python3 figure.py'
         }
      }
      stage('Build2') {
         agent {
            docker {
               image 'blang/latex:ubuntu'
            }
         }
         steps {
             sh 'xelatex sample.tex'
         }
      }
   }
}