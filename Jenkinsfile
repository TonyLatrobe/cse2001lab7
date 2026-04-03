pipeline {
    agent any
    stages {
        stage('Deploy Demo App') {
            steps {
                script {
                    checkout scm  // checks out the repo
                    // Apply the demo-app YAML from the same repo or volume
                    sh 'microk8s kubectl apply -f k8s/demo-app/ -n observability'
                }
            }
        }
    }
}