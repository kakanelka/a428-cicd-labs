node {
    stage('Build') {
        // Define Docker agent
        docker.image('node:16-buster-slim').inside('-p 3000:3000') {
            // Run npm install
            sh 'npm install'
        }
    }
    stage('Test') {
        // Run test.sh script
        sh './jenkins/scripts/test.sh'
    }
}