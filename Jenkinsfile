pipeline {
    agent any  // Chạy trên bất kỳ agent nào có sẵn

    stages {
        stage('Checkout') {
            steps {
                // Kiểm tra mã nguồn từ Git repository
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // Chạy lệnh build
                echo 'Building the project...'
                sh 'chmod +x ./phuong.sh'  // Thay thế bằng lệnh build của bạn
            }
        }
        stage('Test') {
            steps {
                // Chạy kiểm thử
                echo 'Running tests...'
                sh 'chmod +x phuong.sh'  // Thay thế bằng lệnh kiểm thử của bạn
            }
        }
        stage('Deploy') {
            steps {
                // Triển khai ứng dụng
                echo 'Deploying the project...'
                sh 'chmod +x ./phuong.sh'  // Thay thế bằng lệnh triển khai của bạn
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
        always {
            echo 'This will always run.'
        }
    }
}

