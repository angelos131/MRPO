pipeline {
    agent any
    environment {
        MY_GLOBAL_VARIABLE = 'value'
        ANOTHER_VAR = 'test'
    }
    stages {
        stage('Example') {
            steps {
                echo "Значение моей глобальной переменной: ${env.MY_GLOBAL_VARIABLE}"
                echo "Другая переменная: ${ANOTHER_VAR}"
            }
        }
        stage('Build') {
            steps {
                echo "Все еще доступна: ${env.MY_GLOBAL_VARIABLE}"
                sh 'echo $MY_GLOBAL_VARIABLE'
            }
        }
    }
}
