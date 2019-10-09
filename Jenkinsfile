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
            sh 'sh compile'
            git 'https://github.com/narendrasingamaneni91/ecommerce.git'
          }
        }
        stage('test') {
          steps {
            sh 'sh compile'
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