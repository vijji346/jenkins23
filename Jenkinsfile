pipeline {
    agent any
    tools {
        maven 'Apache Maven 3.9.1'
		
    }

    stages {
        stage('git clone') 
		{
            steps {
              git credentialsId: 'github', url: 'https://github.com/kartikeyapro/ks.git'
            }
		}
        stage('Maven Clean') 
		{
            steps {
			sh 'maven clean'
            }
	    }
        stage('Maven Test') 
		{
            steps {
			sh 'maven test'
            }
		}
        stage('Maven Compile') 
		{
            steps {
			sh 'maven compile'
               
            }
		}
		stage('Maven Package')  
		{
            steps {
            sh 'maven package'
            }
        }	 
    }
}

