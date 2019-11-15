pipeline {
        agent any
        stages {
        stage('First') {
                steps {
                echo  env.rule="True"
                }
        }
        stage('Second'){
                steps{
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
