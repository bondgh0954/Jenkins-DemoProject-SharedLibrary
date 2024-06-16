#!/user/bin/env groovy

library identifier: 'shared-library-repo@master', retriever:modernSCM(
[$class: 'GitSCMSource',
remote: 'https://github.com/bondgh0954/shared-library-repo.git',
credentialsId: 'github-credentials'])_
pipeline{
  agent any
  tools{
    maven 'maven-3'
  }
  stages{
    stage('build jar'){
      steps{
        script{
          sh 'mvn package'
        }
      }
    }
    stage('building image'){
      steps{
        script{
          buildImage 'nanaot/java-app:sl3.1'
          dockerLogin()
          pushImage 'nanaot/java-app:sl3.1'
        }
      }
    }

  }

}
