def Ip = ["120.78.143.199","120.79.229.222","120.79.150.67"]

node {
   stage('git code'){
       git credentialsId: '1374fff2-a127-42ba-80d9-43aeeb9214b2', url: 'http://coding.sibu.cn/php/bodyfat.git'
       sh 'pwd'
   }
   stage('copy CODE'){
       for (i in Ip){
           sh "scp -r /home/tomcat/.jenkins/workspace/PHP_deploy/* root@$i:/opt/www/bodyfat"
       }
   }
   stage('chown'){
       for (i in Ip){
           sh "ssh root@$i 'chown -R nginx.nginx /opt/www/bodyfat'"
       }
   }
   stage('Delete .git'){
       for (i in Ip){
           sh "ssh root@$i 'rm -rf /opt/www/bodyfat/.git'"
       }
       
   }
}