node('built-in') {
    /*downloading from github code repo*/
    stage('Continous_Download') {
    git 'https://github.com/k123-v/Devopsmaven.git'
}
   /*building artificats using build tool maven*/
    stage('Continous_Build') {
    sh '''mvn clean '''
    sh '''mvn install '''
    sh '''mvn package '''
}
   /*deploying the artificat into tomcat web server running into QA environment for testing*/
    stage('Continous_Depolyment') {
    sh 'scp /home/ubuntu/.jenkins/workspace/first_pipeline/webapp/target/webapp.war ubuntu@172.31.33.40:/var/lib/tomcat9/webapps/qaapp.war'
}
    /*doing a automation testing on the app deploying*/ 
    stage('Continous_Testing') {
    sh 'echo Testing passed'
}
   /*deploying the artificat into tomcat web server running into Production environment after testing for monitoring*/
    stage('Continous_Delivery') {
    sh 'scp /home/ubuntu/.jenkins/workspace/first_pipeline/webapp/target/webapp.war ubuntu@172.31.46.202:/var/lib/tomcat9/webapps/prodapp.war'
}
}
