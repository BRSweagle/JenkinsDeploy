pipeline {
  agent any
  stages {
    stage('Upload Config') {
      steps {
        SWEAGLEExport(actionName: 'GetConfig', mdsName: 'Client-PRD', fileLocation: '/Users/boondock/Documents/GitHub/JenkinsDeploy/Client-PRD.yaml', exporter: 'all', format: 'yaml')
      }
    }
  }
}