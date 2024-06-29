step 1: 
    Create a perameter store in aws 
Step 2: 
    Update the Code file containing the perameters
Step3:
  Execute this command
    aws ssm get-parameters --region us-east-1 --names project1 --with-decryption --query Parameters[0].Value --output text | tr -d '"' | tr '\\n' '\n' > .env
Step 4: 
    Load the env file in code section
