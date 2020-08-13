pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2 --env HTTP_PROXY=http://child-prc.intel.com:913 --env HTTPS_PROXY=http://child-prc.intel.com:913'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
