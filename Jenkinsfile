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
        stage('compile') {
          steps {
            bat 'mvn compile'
          }
        }
        stage('test') {
          steps {
            bat 'mvn test'
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