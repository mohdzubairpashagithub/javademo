pipeline{
    agent { label "agent01" }
    stages{
        stage("checkout the code") {
            steps{ 
               checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/cloud-dev-user/javademo.git']])   
        }
        }
        stage("build the code") {
            steps{ 
                
                sh " mvn clean package"
            }
        }
        
    }
}
