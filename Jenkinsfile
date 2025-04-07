pipeline{
    
    agent any 
    tools (maven "M3")
    stages(
        
        stage("checkout"){
            
            steps{
                
                git branch: "main", url: "https://github.com/Abraham-AC84/SpringPetClinic.git"
            }
        }
        stage("buld"){
            
            steps {
                
                sh "mvn compile"
            }
        }
        stage("test"){
            
            steps {
                
                sh "mvn test"
            }
        }
        stage("package"){
            
            steps{
                
                sh "mvn package"
            }
        }
        stage("deploy"){
            
            steps{
                
                sh "java - jar /home/coder/.jenkins/workspace/PetClinicDeclarative/target/*.jar"
            }
        }
        
    )
}
