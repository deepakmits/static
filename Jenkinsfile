pipeline {
  agent any 
  stages {
    stage('Upload to AWS.') {
      steps {
          withAWS(region:’us-west-2’,credentials:’pipeline’) {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’deep-jenkins-pipeline’)
          }
        }
    }
  }
}
