pipeline{

agent any
tools{
gradle 'Gradle'
jdk 'JDK'
}
stages{
stage('Check Out'){
steps{
git branch: 'master' , url:'https://github.com/TATIKONDASOWMYA/MyGradleApp01.git'
}
}
stage('Build'){
steps{
sh 'gradle build'
}
}
stage('Test'){
steps{
sh 'gradle test'
}
}
stage('Run'){
steps{
sh 'gradle run'
sh 'gradle Hello'
}
}
}
post{
success {
echo 'Build successful'
}
failure{
echo 'BUild failure'
}
}
} 

