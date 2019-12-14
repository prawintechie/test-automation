pipeline {
    agent {
      docker {
        image 'kdvolder/mvn-plus-npm'
      }
    }

    stages {
        stage ('Packaging Stage') {
            steps {
                sh "mvn clean package -f my-cd/pom.xml"
            }
        }
        stage ('Deployment Stage') {
            steps {
                
            }
        }
    }
    post {
      always {
        cleanWs()
      }
    }
}