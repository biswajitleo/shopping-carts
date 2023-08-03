pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the maven build job'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'this is the maven test job'
        sh 'mvn clean test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the maven package job'
        sh 'mvn package -DskipTests'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}