#!/user/bin/env groovy

@Library('jenkins-shared')_
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
