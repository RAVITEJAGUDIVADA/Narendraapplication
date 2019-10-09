pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/RAVITEJAGUDIVADA/Narendraapplication.git', branch: 'master')
      }
    }
    stage('compile') {
      parallel {
        stage('Compile') {
          steps {
            sh 'compile'
          }
        }
        stage('test') {
          steps {
            sh 'mvn test'
          }
        }
      }
    }
    stage('build') {
      steps {
        bat 'mvn package'
      }
    }
  }
}