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
stage('terraform destroy'){ steps{
sh label: '',script: 'terraform destroy --auto-approve' 
}
}
}
}
