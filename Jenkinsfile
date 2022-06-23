pipeline{
    agent any
    stages {

    stage('build'){
    steps{
    sh 'ant -f build.xml -v'
    }
    }
 stage(‘test’){
    steps{
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
