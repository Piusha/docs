# Serverless Code Glossary 
### Crete serveless app

    $ serverless create -t aws-nodejs
- -t  --template = Serverless Template

### Run on local

In order to run serverless app in local  you need to import serverless-offline npm pacckage. After that in command line you can execute

	$ npm install serverless-offline --save-dev

    $ serverless invoke local -f <function name> -d <event object data>
    
- -f = function name
- -d = Event data String or Object as a String

### create aws profile 

serverless config credentials --provider aws --key <KEY> --sercret <SECRET>

### Deploy on AWS

Deploy dev

    $ serverless deploy --aws-profile <profile>
    Or 
    $ sls deploy --aws-profile <profile>

Deploy Production
    
    $ sls deploy -s production -f hello
    
Remove Serverless

    $ sls remove -s dev --aws-profile <profile>
    
- -s stage

### Serverless Log

    $ sls logs -f <function name> -s <stage> -t
    
- -f function name
- -s stage/ env
- -t tail (loga tial)