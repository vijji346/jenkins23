pipeline {
    agent any
    tools {
        maven ' Apache Maven 3.9.1 '
		
    }

    stages {
        stage('git clone') 
		{
            steps {
              git credentialsID: 'github' , url: 'https://github.com/vijji346/april23.git'
            }
			}
	    stage('Code Clean') 
		{
            steps {
			sh 'mvn clean'
            }
			}
        stage('Code Validate') 
		{
            steps {
			sh 'mvn validate'
            }
			}
        stage('Code Compile') 
		{
            steps {
			sh 'mvn compile'
               
            }
		    }
		stage('Code Test')  
		{
            steps {
            sh 'mvn test'
            }
            }
        stage('Code package')  
		{
            steps {
             sh 'mvn package'
            }
            }			 
}
}

