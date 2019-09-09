pipeline {
  agent any
  stages {
    stage('Upload Config') {
      parallel {
        stage('Upload Config') {
          steps {
            SWEAGLEExport(actionName: 'GetConfig', mdsName: 'Client-PRD', fileLocation: '/Users/boondock/Documents/GitHub/JenkinsDeploy/Client-PRD.yaml', exporter: 'all', format: 'yaml')
          }
        }
        stage('Git') {
          steps {
            sh 'git pull'
          }
        }
        stage('push') {
          steps {
            sh '''git push
git commit'''
          }
        }
      }
    }
  }
}