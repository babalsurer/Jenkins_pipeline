pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'apache-maven-3.5.4'){
                        sh "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'apache-maven-3.5.4'){
                        sh "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'apache-maven-3.5.4'){
                        echo "do u wnat aprrove"
                        sleep 1
                        sh "mvn deploy"
                        
                }

            }
        }
    }
}
