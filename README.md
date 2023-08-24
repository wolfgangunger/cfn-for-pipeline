# cfn-for-pipeline
repo for cfn templates for codepipeline deployment  
  
## structure
each template must be in a subfolder names cfn_xxx  
  
each subfolder must contain a cfn template named template.yaml and the parameter jsons  
one json for each environment , named params_[stage].json  

example :   
cfn_001_simple_user  
-template.yaml  
-params_dev.json  
-params_qa.json  
-params_prod.json  

you should layer your cloudformation templates according to common stacks that provide outtputs for other stacks and the stacks using   
other stacks outputs to be deployed later on, like for example :  
001-099 IAM  
100-199 VPC and Network  
200-299 Storage and DB  
300-399 Compute Services  
400-499 Container Service   
500-599 Monitoring   
etc   

