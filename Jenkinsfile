#!groovy
node {
   // Mark the code checkout 'stage'....
   stage ('Checkout'){

      // Get some code from a GitHub repository
      checkout scm
      // Get the maven tool.
      // ** NOTE: This 'maven3' maven tool must be configured
      // **       in the global configuration.
      def mvnHome = tool 'maven3'
   }

   // Mark the code build 'stage'....
   stage ('Build Maven'){
      // Run the maven build
      sh "${mvnHome}/bin/mvn clean install"
   }
}
