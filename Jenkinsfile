pipeline {
    agent any
	 tools {
        jdk 'jdk'
        nodejs 'node'
    }
	
	 environment {
        	SCANNER_HOME = tool 'sonar'
    	}
	
    stages {
        stage('testing') {
            steps {
                script {
			sh 'echo "Starting the testing step...."'
                }
            }
        }
	    
	stage('testing-sonar'){

		steps{
			sh 'pwd'
			sh 'ls /var/lib/jenkins/tools/hudson.plugins.sonar.SonarRunnerInstallation/sonar/bin/'
		}
		// steps{
		// 	withSonarQubeEnv('sonar') {
  //                   	sh '''$SCANNER_HOME/bin/sonar-scanner -Dsonar.projectName=react\
  //                   	-Dsonar.projectKey=react'''
  //               	}		
  //      		}	
	}
	// stage("quality gate") {
 //          	  steps {
 //                	script {
 //                   		 waitForQualityGate abortPipeline: false, credentialsId: 'sonar'
 //                }
 //            }
 //        }
	        
        // stage('build') {
        //     	steps {
        //         	sh 'npm cache clean --force'
        //         	sh 'npm ci'
        // 	    }
	       //  }

     }
}
