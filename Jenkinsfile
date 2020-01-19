node
{
stage 'Build'
   // Run the maven build
   def mvnHome = tool 'm6'
   sh "${mvnHome}/bin/mvn clean test sonar:sonar"
   step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
}
