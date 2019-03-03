pipeline {
    agent any 
    tools {
        jdk 'JAVA'
        maven 'MAVEN'
    }

    stages {
        stage('clone-repo') {
         
            steps {
                
                sh 'git clone https://github.com/trinada/simple-java.git'
                sh 'mvn clean -f simple-java '
            }
        }
        stage('Test') {
             
            steps {
                sh 'mvn test -f simple-java'
                echo 'test completed'
            }
        } 
        stage('Build'){
           steps{
               sh 'mvn install package -f simple-java'
               echo "build completed"
           }
    
            
        }
    }
    
    }
