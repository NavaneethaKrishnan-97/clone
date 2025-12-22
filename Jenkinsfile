pipeline
{
agent any
parameters
	{
		booleanParam(name: 'SKIP_TEST', defaultValue: false, description: 'Skip the test stage')
	}
stages
	{
		stage('Build')
		{
			steps
				{
					echo('Build app')
				}
		}
		stage('Execute')
		{
			steps
				{
					echo('Execute app')
				}
		}
		stage('Test')
		{
			when
			{
				expression{ return !params.SKIP_TEST }
			}
			steps
				{
					echo('Test app')
				}
		}
		stage('Deploy')
		{
			steps
				{
					echo('Deploy app')
				}
		}
	}
}
