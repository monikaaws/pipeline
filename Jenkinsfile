pipeline{
agent any
stages{
stage('one'){
steps{
echo "this is build stage"
}
stage('two'){
steps{
input("do you want to proceed")
}
stage('three'){
steps{
when{
not{
branch "master"
}
}
steps{
echo "hello"
}
}
}
stage('four'){
parallel{
stage('unit test'){
steps{
echo "running unit test"
}
}
}
}

