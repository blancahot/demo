pipeline {
  triggers {
    githubPush(githubOrg: 'public', branchRegex: 'main')
  }

  agent any

  stages {
    stage('Build & Run Docker') {
      steps {
        docker-compose up --build -d
      }
    }
  }
}