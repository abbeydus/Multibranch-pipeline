pipeline{
  agent any
  stages{
  	stage('version-control'){
  		steps{
  			checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/abbeydus/Multibranch-pipeline.git']]])
  		}
  	}
    stage('parallel-job'){
      parallel{
        stage('sub-job1'){
          steps{
            echo 'action1'
            echo 'fix me'
      develop
            echo 'see you'
            echo ' see you'
            main
          }
        }
        stage('sub-job2'){
          steps{
            echo 'action2'
            echo 'hello me'
            echo 'sup'
            echo 'hello'
          }
        }
      }
    }
    stage('codebuild'){
    	steps{
    		sh 'cat /etc/passwd'
    	}
    }
  }
}
