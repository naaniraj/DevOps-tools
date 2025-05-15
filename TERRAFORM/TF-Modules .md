## creating EC2 instence 
___________________________

    provider "aws" {
      region     = "us-east-1"
      access_key = "q28gjkaur4hdi"
      screct_key = "n5ujsolrj845tgbn7654edv8766789olk"
    }
    resources "aws_instence" {
      ami       = "ami-i9ij54ed9olkjewsdfg765r"
      instence_type = "t2.medium"
      tages {
        name = "web-server"
      }   
    }  
