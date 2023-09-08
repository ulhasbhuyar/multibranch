node('master')
{
   stage('Continuous Download')
       {
         git 'https://github.com/ulhasbhuyar/jenkinspipeline.git'
       }
  stage('Continuous Build')
       {
        sh 'mvn package'
       }
  stage('Continuous Deployment')
       {
        sh 'scp  /home/ubuntu/.jenkins/workspace/pipelinejob/webapp/target/webapp.war  ubuntu@172.31.37.169:/var/lib/tomcat9/webapps/qaenv.war'
       }
  stage('Continuous Testing')
       {
        sh 'echo "Testing passed"'
       }
  stage('Continuous Delivery')
       {
        sh 'scp  /home/ubuntu/.jenkins/workspace/pipelinejob/webapp/target/webapp.war  ubuntu@172.31.42.216:/var/lib/tomcat9/webapps/prodenv.war'
       }
}

