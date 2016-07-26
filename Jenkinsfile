node {
	stage 'Checkout'
	checkout scm

    stage 'Build'
    sh "/usr/local/bin/nuget restore"
    sh "/Applications/Xamarin\\ Studio.app/Contents/MacOS/mdtool build -t:Build -c:Debug\\|iPhoneSimulator -p:JenkinsTest.iOS JenkinsTest.sln"
}