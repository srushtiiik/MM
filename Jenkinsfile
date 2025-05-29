Pipeline{
  any agent
    tools{
      maven 'Maven'
      }
      stages{
        stage('Checkout'){
          step{
          	git branch:'master',url :'https://github.com/srushtiiik/MM.git'
          }
         }
        stage('Build'){
          step{
            sh 'mvn compile package'
            }
           }
         stage('Test'){
           step{
             sh 'mvn test'
             }
            }
          stage('Run application'){
            step{
               sh 'java -jar target/MM-1.0-SNAPSHOT.jar'
               }
              }
          }
       post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
            	
        
