pipeline {
        agent any
        stages {
        stage('First') {
                steps {
                sh 'echo "Step One"'
		echo env.EXECUTE="True"
                }
        }
        stage('Second'){
                steps {
                sh 'echo "Step Two"'
		sh 'echo "Updating Second Stage"'
		}
		when{
		enviroment name: 'EXECUTE',
		value:'True'
                }
        }
        stage('Third') {
                steps {
                sh 'echo "Step Three"'
                }
		when{
                enviroment name: 'EXECUTE',
                value:'False'
                }
        }
        }
}
