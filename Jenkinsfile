node
{
stage 'Checkout'
        
   def mvnHome = tool name: 'M3', type: 'maven'

stage 'Build'
     
   sh "${mvnHome}/bin/mvn clean test sonar:sonar"
   step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
}
