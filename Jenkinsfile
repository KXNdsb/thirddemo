pipeline {
    agent any
    stages {
        stage('Git-Checkout') {
			steps {
				echo "获得资源库 ";
				git branch: 'main', url: 'https://github.com/KXNdsb/thirddemo.git'
			}
		}
        stage('test') {
            steps {
                echo 'build test'
                bat 'python --version'
                bat 'pip install flask pytest'
                bat 'export pythonpath=src;pytest'
            }
        }
    }
}
