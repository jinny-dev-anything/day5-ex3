pipeline {
    agent none
    stages {
        stage('Parallel Build & Test') {
            parallel {
                stage('Build on Agent1') {
                    agent { label 'agent1' }
                    steps {
                        sh 'echo "Agent1 빌드 수행 중..."'
                        sh 'sleep 5'
                        sh 'echo "Agent1 빌드 완료!"'
                    }
                }
                stage('Test on Agent2') {
                    agent { label 'agent2' }
                    steps {
                        sh 'echo "Agent2 테스트 수행 중..."'
                        sh 'sleep 5'
                        sh 'echo "Agent2 테스트 완료!"'
                    }
                }
            }
        }
    }
}
