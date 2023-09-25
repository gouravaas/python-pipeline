pipeline {
	agent {
		label "Pipeline-slave"
	}
	stages{
		stage ("pull scm"){
			steps {
				git branch: 'python', url: 'https://github.com/gouravaas/python-pipeline.git'	
			}
		}
		stage ("Build"){
			steps {
				sh 'python -v'
				sh 'python cp.py'
			}
		}
		stage ("test"){
			steps {
				sh 'python test.py'
			}
		}
	}
}
