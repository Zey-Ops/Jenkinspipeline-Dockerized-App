pipeline {
    agent { label 'master' }

    environment {
        ECR_REGISTRY = ''

    }

    stages {
        stage('Create ECR repo') {
            steps {
                echo 'Creating ECR Repo'
            }
        }

        stage ('Build App Docker Images') {
            steps {
                echo 'Build app docker images'
            }
        }

        stage ('Pushing Docker image to ECR repo') {
            steps {
                echo 'Pushing images to ECR'
            }
        }

        stage ('Creating infastructure for the app') {
            steps {
                echo 'Creating Docker Swarm'
            }
        }

        stage ('Test the infastructure') {
            steps {
                echo 'Testing if Docker swarm is ready'
            }
        }

        stage ('Deploy the application') {
            steps {
                echo 'Deplot the app'
            }
        }

        stage ('Test the application') {
            steps {
                echo 'Check if the application is ready or not'
            }
        }
    }

    post {
        always {
            echo 'Deleting all local images'
        }

        failure {
            echo 'Delete the image repo on ECR due to failure'
            echo 'Delete the cloudformation stack due to failure'
        }
    }
}
