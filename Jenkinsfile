pipeline {
  agent any

  stages {
    stage("build") {
      steps {
        
        echo "building now. will call browseratck..."
        browserstack(credentialsId: 'e620e0e1-e1f5-48a3-9775-7dbec8cd3322	') {
          echo "called browserstack. inside the callback..."
          // browserStackReportPublisher("this is the value of some value")
          echo "BROWSERSTACK_LOCAL value inside browserstack: ${BROWSERSTACK_LOCAL}"
          // BROWSERSTCK_BUILD_NAME = BUILD_TAG

        }

        // echo "uploading the app first"

        // browserstackAppUploader('/Users/chaugs_rohan/Downloads/Instagram_v157.0.0.37.120_apkpure.com.apk') {
        //     // some block
        //     echo "BROWSERSTACK_APP_ID: ${BROWSERSTACK_APP_ID}"
        // }
      }
    }

    // stage("test") {
    //   steps {
    //     echo "testing now..."
    //   }
    // }

    // stage("deploy") {
    //   steps {
    //     echo "deploying now..."
    //   }
    // }
  }

  // post {
  //   always {
  //     echo "calling the publisher pipeline..."
  //     // browserStackReportPublisher "app-automate"
  //   }
  // }
}