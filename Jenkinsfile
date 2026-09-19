pipeline {
    agent any

    stages {
        stage('Run Tests') {
            steps {
                bat '"C:\\Program Files\\Python313\\python.exe" -m pytest -v --alluredir=allure-results'
            }
        }
    }
 post {
        always {
            allure includeProperties: false,
                   jdk: '',
                   results: [[path: 'allure-results']]
        }
    }
}
