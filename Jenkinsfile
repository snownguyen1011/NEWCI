pipeline {
  agent any
  stages {
    stage('SCM-Checkout') {
      parallel {
        stage('SCM-Checkout') {
          steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'ravi', url: 'https://github.com/snownguyen1011/NEWCI.git']]])
          }
        }
        stage('Validating Jenkinsfile') {
          steps {
            validateDeclarativePipeline '/var/lib/jenkins/workspace/NEWCI_master-VIG6SFZFSE5Q75WN6JARQS22S2QDY5YYLLLRDXPZTU4RJWVJNSYQ/Jenkinsfile'
          }
        }
      }
    }
    stage('Build') {
      steps {
        sh '''cd /var/lib/jenkins/workspace/NEWCI_master-VIG6SFZFSE5Q75WN6JARQS22S2QDY5YYLLLRDXPZTU4RJWVJNSYQ/{project-name}/
mvn clean install'''
      }
    }
  }
}