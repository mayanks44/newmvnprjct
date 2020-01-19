node
{
stage 'Build'
   // Run the maven build
   sh "mvn clean test sonar:sonar"
   step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
}
