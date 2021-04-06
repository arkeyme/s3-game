Do this and find STANDARD_IA in a output:   

     aws s3api list-objects --bucket s3game-level10-gac6tf83erp6 --profile s3-game > all_objects

Or:   

     aws s3api list-objects --bucket s3game-level10-gac6tf83erp6 --profile s3-game --query 'Contents[?StorageClass == `STANDARD_IA`]'

It is not obvious how content query working with aws cli, and official documentation does not cover it. Since, this is not a topic of the course, I googled the solution. 