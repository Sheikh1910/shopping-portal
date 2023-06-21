pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'this is the build the app job'
        sh 'npm install'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'this is the test the job'
        sh 'npm test'
      }
    }

    stage('package-the-app') {
      steps {
        echo 'this is the package the app job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}