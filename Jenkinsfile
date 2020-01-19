node
{
stage 'Build'
   // Run the maven build
   export MAVEN_HOME=/usr/share/maven
   export PATH=$PATH:$MAVEN_HOME/bin
   mvn --version
   sh "mvn clean test sonar:sonar"
   step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
}
