node {
    stage('pull repo') { 
        git branch: 'dev1', url: 'https://github.com/saaaneo/Jenkins-.NET-Core-CI-CD-pipeline.git'
    }
    stage('Restore packages') {
                sh 'dotnet restore WebApplication.sln'
            }
    stage('Clean') {
               sh 'dotnet clean WebApplication.sln --configuration Release'
            }
    stage('Build') {
		sh 'dotnet build WebApplication.sln --configuration Release --no-restore'
	}
    stage('Publish') {
		sh 'dotnet publish WebApplication/WebApplication.csproj --configuration Release --no-restore'
	}
}
