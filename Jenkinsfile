pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/2025sl93099-s/labsheet1-2025sl93099.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Build Stage'
                sh 'python3 --version'
            }
        }

        stage('Test') {
            steps {
                sh '''
                python3 - <<EOF
import calculator

assert calculator.add(2,3) == 5
assert calculator.sub(5,3) == 2
assert calculator.mul(2,3) == 6
assert calculator.div(6,3) == 2
print("All tests passed")
EOF
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploy Stage (dummy for now)'
            }
        }
    }
}
