node {
	stage 'Checkout'
	checkout scm

    stage 'Restore packages'
    sh "/usr/local/bin/nuget restore"

    stage 'iOS Build'
    sh "/Applications/Xamarin\\ Studio.app/Contents/MacOS/mdtool build -t:Build -c:Debug\\|iPhoneSimulator -p:JenkinsTest.iOS JenkinsTest.sln"

    stage 'Android Build'
    sh "/usr/local/bin/xbuild Droid/JenkinsTest.Droid.csproj /p:Configuration=Release /t:SignAndroidPackage"
}