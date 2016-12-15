node {
   // Mark the code checkout 'stage'....
    job('Multibranch_Workflow_Test_checkout') {

      // Checkout code from repository
      checkout scm
   }

   // Get the maven tool.
   // ** NOTE: This 'M3' maven tool must be configured
   // **       in the global configuration.
   // def mvnHome = tool 'M3'

   // Mark the code build 'stage'....
    job('Multibranch_Workflow_Test_Build') {
       // Run the maven build
       maven {
           mavenInstallation('Maven 3')
           goals('clean install -DskipTests')
           mavenOpts('-Xrs -Xmx1024M -Xss20M -XX:MaxPermSize=1024M -XX:ReservedCodeCacheSize=64M -XX:+UseGCOverheadLimit')
           rootPOM('pom.xml')
       }
   }
}
