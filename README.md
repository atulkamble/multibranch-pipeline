### multibranch-pipeline

### Clone this Repository
```
git clone
cd 
```

Steps to follow

1. Create public repo
2. copy link of it
example: https://github.com/atulkamble/multibranch-pipeline.git
3. Jenkins server >> New Item >> Multibranch Pipeline
scm >> git >> pasted github repo link 
example: https://github.com/atulkamble/multibranch-pipeline.git
create 
4. add Jenkinsfile
```
pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add build steps here, e.g., compile code, run tests, etc.
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add test steps here, e.g., unit tests, integration tests, etc.
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deployment steps here, e.g., deploy to server, etc.
            }
        }
    }
}
```
```
git add .
git commit -m "code"
git push origin main
```
5. ```
   git checkout
   ```
6. * crosscheck current branch as new
```
git checkout -b new 
```
7. Update Readme file
```
git add .
git commit -m "updated readme"
git push --set-upstream origin new
```
8. Crosscheck branches on Jenkins Server
9. Scan multibranch-pipeline
