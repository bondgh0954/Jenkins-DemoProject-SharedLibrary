#!/user/bin/env groovy

@Library('jenkins-shared')
pipeline{
  agent any
  tools{
    maven 'maven-3'
  }
  stages{
    stage('build jar'){
      steps{
        script{
          buildJar()
        }
      }
    }
    stage('build image'){
      steps{
        script{
          buildImage 'nanaot/java-app:sl.1'
          dockerLogin()
          pushImage 'nanaot/java-app:sl.1'
        }
      }
    }
  }
}