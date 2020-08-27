pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "maven"
   }

   environment {
      AXWAY_APIM_CLI_HOME = '/var/jenkins_home'
   }

   stages {
      stage('Build') {
         steps {
            // Get the repository from GitHub
            git 'https://github.com/cbrowet-axway/recipes-api-project.git'

            // Run Maven 
            sh "mvn clean exec:java"
         }
      }
   }
}