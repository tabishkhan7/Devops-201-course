node {
   def mvnHome
   def app
   stage('Checkout') { 
      git 'https://github.com/tabishkhan7/Devops-201-course.git'
      mvnHome = tool 'MAVEN_HOME'
   }
   
stage ('Build') {
       sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
   }
/*
stage ('Docker Image Build') {
       app = docker.build("tabishkhan7/devops201:${BUILD_NUMBER}")
}

stage ('Push Docker Image') {
       docker.withRegistry('https://registry.hub.docker.com','docker-credential') {
        		app.push("1-${BUILD_NUMBER}")
        		app.push("latest")
      	}
}
   

stage('Run Container') {
      sh "docker run -p 8082:8080 -d tabishkhan7/devops201"
}
*/
}
