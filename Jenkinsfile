pipeline{
    agent any
    stages {

    stage('build'){
    Steps{
    sh 'ant -f build.xml -v'
    }
    }
 stage(‘test’){
    Steps{
    sh 'echo “This is blue”'
    }
    }

    }
    post {
   	 always{
   		 archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
   	 }
    }
}
