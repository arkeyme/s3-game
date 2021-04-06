Do this and find STANDARD_IA in a output:   
     aws s3api list-objects --bucket s3game-level10-gac6tf83erp6 --profile s3-game > all_objects
Or:   
     aws s3api list-objects --bucket s3game-level10-gac6tf83erp6 --profile s3-game --query 'Contents[?StorageClass == `STANDARD_IA`]'