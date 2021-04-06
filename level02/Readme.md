    
    aws configure --profile s3-game

Since this is not MY keys and these keys are already exposed to the world by game's author, I left them as is in command output:

    aws configure --profile s3-game
    AWS Access Key ID [None]: AKIAZBIEGK7GRYHVNWVB
    AWS Secret Access Key [None]: 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
    Default region name [None]: us-east-2
    Default output format [None]:

    aws s3api get-object --bucket s3game-level2 --key treasure2 --profile s3-game treasure2
    cat treasure2