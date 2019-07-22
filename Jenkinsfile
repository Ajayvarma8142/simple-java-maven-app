pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/Ajayvarma8142/simple-java-maven-app.git', branch: 'master')
      }
    }
    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            bat 'mvn install'
          }
        }
        stage('junit-test') {
          steps {
            bat 'mvn test'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        bat 'REM'
      }
    }
  }
}