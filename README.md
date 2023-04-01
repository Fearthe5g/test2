# test2
 name: My cookl WorkFlow

on:
   push:
   push_request:
   workflow_dispatch:
   
jobs:
  myfirtstjob:
            name: First job
            runs-on: ubuntu-latest
            steps:
              -name: Step One
               uses: actions/checkout@v3
               -name: Step Two
               run:
                  touch newfile.yaml
                  echo "Please Andres is Friday let me go" >> newfile.yaml
                  cat newfile.yaml
                  pwd
                  
     mysecondjob:
              needs: [myfirstjob]
              name: Secondjob
              runs-on: macos-latest
              steps:
              -name: step one
              run: date
              
     mythirdjob:
            name: Third job
            runs-on: Windoes-latest
            steps:
            -name: Step One
            run: date
  
