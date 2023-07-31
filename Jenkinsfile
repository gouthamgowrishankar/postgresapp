pipeline {
  agent any
  tools {
        maven "$maven"
    }
  stages {
    stage('Deploy CloudHub') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('Anypoint.Platform')
      }
      steps {
        sh 'mvn deploy -P cloudhub -Dmule.version=4.4.0 -Danypoint.username=${ANYPOINT_CREDENTIALS_USR} -Danypoint.password=${ANYPOINT_CREDENTIALS_PSW}' 
      }
    }
  }
}