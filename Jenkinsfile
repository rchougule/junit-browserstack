pipeline {
  agent any

  stages {
    stage("build") {
      steps {
        
        echo "building now. will call browseratck..."
        browserstack(credentialsId: 'e8a4ff63-716f-413d-a70d-5b8665c9b8e2') {
          echo "called browserstack. inside the callback..."
          // browserStackReportPublisher("this is the value of some value")
          echo "BROWSERSTACK_LOCAL value inside browserstack: ${BROWSERSTACK_LOCAL}"

        }

        // echo "uploading the app first"

        // browserstackAppUploader('/Users/chaugs_rohan/Downloads/Instagram_v157.0.0.37.120_apkpure.com.apk') {
        //     // some block
        //     echo "BROWSERSTACK_APP_ID: ${BROWSERSTACK_APP_ID}"
        // }
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
      browserStackReportPublisher("automate")
    }
  }
}