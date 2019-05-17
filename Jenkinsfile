node {
   stage('Cluster Off') {
        sh '/data/script/1slb12'
        sh '/data/script/2slb12'
##		sh 'ansible NG -m shell -a 'sed -i ''
   }
   stage('Deploy') {
       echo "stop tomcat"
       echo "mv package"
       echo "copy package"
       echo "检查api"
       echo "修改Cluster"
       echo "start tomcat"

   }
   stage('Cluster On') {
       sh '/data/script/aslb'

   }
}