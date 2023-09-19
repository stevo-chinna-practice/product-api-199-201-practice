pipeline {

  agent any

  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          echo "******* Munit test cases execution ********"
      }
    }

     stage('Deployment') {

      steps {
            bat 'mvn -U -V -e -B -DskipTests -Dusername=Stevo2306 -Dpassword=Stevo2306 -Danypoint.platform.client_id=013b3c2b892f46c2b11e40a520ecaf38 -Danypoint.platform.client_secret=15812d9a646E4904a783c94FDa6A9C08 -Pdev deploy -DmuleDeploy'
    }
   }
  }
 }