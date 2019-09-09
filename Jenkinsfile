pipeline {
  agent any
  stages {
    stage('Build Files') {
      parallel {
        stage('Build Files') {
          steps {
            sh '''echo 
curl -X POST https://testing.sweagle.com/api/v1/tenant/metadata-parser/parse -H "Authorization: bearer 783d4f5b-c260-4cce-936e-00d2483875ab" -d "mds=Client-PRD&parser=all&args=&format=YAML" -o /Users/boondock/Documents/GitHub/JenkinsDeploy/Client-PRD.yaml

echo Git add .
echo Git commit -m "Alter File"
echo Git push origin master'''
          }
        }
        stage('error') {
          steps {
            echo 'Build Environment\'s'
            SWEAGLEExport(actionName: 'GetConfig', mdsName: 'Client-PRD', fileLocation: 'https://github.com/BRSweagle/JenkinsDeploy/Client-PRD', exporter: 'all', format: 'JSON')
          }
        }
      }
    }
  }
}