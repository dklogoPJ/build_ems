pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/dklogo/laravel-login-AUTH.git'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'  // Or any other build process you have
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                // Add commands to run tests (if applicable)
                sh 'npm test'
            }
        }
        stage('Static Analysis') {
            steps {
                // Integrate static analysis tools like SonarQube, ESLint, etc.
                sh 'sonar-scanner'
            }
        }
        stage('Security Scan') {
            steps {
                // Integrate security scanning tools like OWASP ZAP, SonarQube, etc.
                 sh 'owasp-zap -cmd <parameters>'
            }
        }
        stage('Deploy') {
            steps {
                // Add commands to deploy your static page
                //copy files to a web server
            }
        }
    }
}
