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
            bat 'mvn compile test install'
          }
        }
        stage('test') {
          steps {
            sh 'sh test'
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