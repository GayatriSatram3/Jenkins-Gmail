pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building..."
            }
        }

        stage('Test') {
            steps {
                echo "Tests Passed"
            }
        }
    }

    post {
        success {
            mail(
                to: 'satramgayatri@gmail.com',
                subject: "Build Successful - ${env.JOB_NAME}",
                body: """
Hello,

The build completed successfully.

Project: ${env.JOB_NAME}
Build Number: ${env.BUILD_NUMBER}

Version is ready for testing.

Regards,
Jenkins
"""
            )
        }
    }
}