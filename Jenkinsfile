pipeline {
 agent { label 'demo' }
 parameters {
     password(name: 'PASSWD', defaultValue: '', description: 'Please Enter your Gitlab password')
 }
 stages {
  stage('Deploy')
  {
    steps { 
        git branch: 'main', credentialsId: 'GitlabCred', url: 'https://gitlab.com/learndevopseasy/devsecops/spingboot-cd-pipeline.git'
         sh "echo LETS-DO-A-DUMMYCHECKIN  >> README.MD "
	 sh 'git commit -a -m "New deployment for Build $IMAGE"'
	 sh "git push https://scmlearningcentre:$PASSWD@gitlab.com/learndevopseasy/devsecops/spingboot-cd-pipeline.git"
    }
  }
 }
}
