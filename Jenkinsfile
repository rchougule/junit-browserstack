pipeline {
  agent any

  stages {
    stage("build") {
      steps {
        echo "building now. will call browseratck..."
        browserstack(credentialsId: '2f42b03a-97dd-41e2-83a8-549718172d92') {
          echo "called browserstack. inside the callback..."
          browserStackReportPublisher("this is the value of some value")
        }
        echo "now again outside..."
      }
    }

    stage("test") {
      steps {
        echo "testing now..."
      }
    }

    stage("deploy") {
      steps {
        echo "deploying now..."
      }
    }
  }

  post {
    always {
      echo "calling the publisher pipeline..."
      // browserStackReportPublisher("this is the value of some value")
    }
  }
}