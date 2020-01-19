node
{
stage 'Build'
   // Run the maven build
   def mvnHome = tool name: 'maven 3.0', type: 'maven'
   sh "${mvnHome} clean test sonar:sonar"
   step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
}
