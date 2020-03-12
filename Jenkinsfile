pipeline {
	agent any
	environment {EXECUTE = true }
	stages {
		stage ('One') {
			steps {
				sh 'echo "step one"'
			}
		}
		stage ('Twoe') {
			when { expression {EXECUTE}}
			steps {
                                sh 'echo "step Two"'
				sh 'echo "Updating Second Stage"'
                        }
                }
		stage ('Three') {
			when { expression {EXECUTE == false}}
			steps {
                                sh 'echo "step Three"'
                        }
                }
	}
}
