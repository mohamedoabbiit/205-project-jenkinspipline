Pipeline {
   stages {
        stage('Create ECR Repo') {
            steps {
                echo 'Creating ECR Repo for App'
            }
        }
        stage('Build App Docker Image') {
            steps {
                echo 'Building App Image'
            }
        }
        stage('Push Image to ECR Repo') {
            steps {
                echo 'Pushing App Image to ECR Repo'
            }
        }
        stage('Create Infrastructure for the App') {
            steps {
                echo 'Creating Infrastructure for the App on AWS Cloud'
            }
        }
        stage('Test the Infrastructure') {
            steps {
                echo "Testing if the Docker Swarm is ready or not, by checking Viz App on Grand Master with Public Ip Address: ${MASTER_INSTANCE_PUBLIC_IP}:8080"
            }
        }
        stage('Deploy App on Docker Swarm'){
            steps {
                echo "Cloning and Deploying App on Swarm using Grand Master with Instance Id: $MASTER_INSTANCE_ID"
            }
        }
    }
}