pipeline {
    agent any 
    stages {
        stage('clone-repo') {
         
            steps {
                
                bat 'git clone https://github.com/trinada/simple-java.git'
                bat 'mvn clean -f simple-java '
            }
        }
        stage(' Test') {
             
            steps {
                bat 'mvn test -f simple-java'
                echo 'test completed'
            }
        }
    }
}
