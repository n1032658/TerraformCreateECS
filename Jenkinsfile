pipeline {

agent any
tools {
  terraform 'terraform'
}
stages{

stage('git checkout'){

steps{
git branch: 'main', credentialsId: 'gitToken', url: 'https://github.com/n1032658/TerraformCreateECS.git'
}

}
stage('terraform init'){
    steps{
sh label: '',script: 'terraform init'
}
}
stage('terraform apply'){ steps{
sh label: '',script: 'terraform apply --auto-approve' 
}
}
}
}
