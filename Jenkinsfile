pipeline {
        agent any
        stages {
        stage('First') {
                steps {
		sh 'echo "Step One"'
                echo  env.rule="False"
                }
        }
        stage('Second'){
                steps{
		sh 'echo "Step Two"'
                sh 'echo "Updating Second Stage"'
                }

                 when {
                        environment name: 'rule',
                        value:'True'
            }
        }
         stage('Three') {
            steps {
                sh 'echo "Step Three"'
            }
                when {
                        environment name: 'rule',
                        value:'False'
            }
        }
	}
}
