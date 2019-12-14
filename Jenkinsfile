pipeline {
    agent {
      docker {
        image 'kdvolder/mvn-plus-npm'
      }
    }

    stages {
        stage ('Packaging Stage') {
            steps {
                sh "mvn clean package -f test-automation/pom.xml"
            }
        }
       
    }
    post {
      always {
        cleanWs()
      }
    }
}