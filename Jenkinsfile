pipeline {
  agent any
  stages {
    stage('SCM-Checkout') {
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'ravi', url: 'https://github.com/snownguyen1011/CICD.git']]])
      }
    }
    stage('Build') {
      steps {
        sh '''cd /var/lib/jenkins/workspace/NEWCI_master-VIG6SFZFSE5Q75WN6JARQS22S2QDY5YYLLLRDXPZTU4RJWVJNSYQ/{PROJECT-NAME}/
mvn clean install'''
      }
    }
  }
}