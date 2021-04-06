
     aws s3 cp s3://s3game-level3 ./ --recursive --profile s3-game
     aws s3api head-object --bucket s3game-level3 --key treasure3_has_no_secret_code --profile s3-game