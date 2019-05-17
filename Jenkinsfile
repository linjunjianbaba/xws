node {
   stage('Cluster Off') {
        sh '/data/script/1slb12'
        sh '/data/script/2slb12'
		sh 'ssh root@112.74.130.92 "hostname"'
		sh 'ssh root@120.77.225.5 "hostname"'
		sh 'ssh root@120.79.106.226 "hostname"'
		sh 'ssh root@120.76.85.30 "hostname"'
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