3.	pipeline {
    agent any
stages {
    // NEW STAGE: Pull the source code first!
    stage('Checkout SCM') {
        steps {
            echo "Pulling code from GitHub..."
            // This 'git' step is provided by the Git Plugin
            git url: 'https://github.com/jenkins-docs/simple-java-maven-app.git', branch: 'main'
        }
    }

    stage('Build') {
        steps {
            // Let's run a real command now that we have the code
            // 'sh' is a step for running a shell command on Linux/macOS
            sh 'ls -la'
            echo "In a real build, we'd run 'mvn clean install'."
        }
    }

    stage('Test') {
        steps {
            echo "Running tests..."
        }
    }

    stage('Deploy to Staging') {
        steps {
            echo "Deploying to staging..."
        }
    }
}
}

