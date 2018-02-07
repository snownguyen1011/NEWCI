pipeline {
  agent any
  stages {
    stage('SCM-Checkout') {
      steps {
        git(url: 'https://github.com/snownguyen1011/CICD.git', branch: 'master', credentialsId: 'ravirajakoineni')
      }
    }
  }
}