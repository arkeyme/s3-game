    aws s3 cp s3://s3game-level6-vjv45x1gux81 ./ --recursive --profile tmp
    aws s3api list-objects --bucket s3game-level6-vjv45x1gux81 --profile tmp

    aws s3api select-object-content --bucket s3game-level6-vjv45x1gux81 --key s3select.csv.gz --expression "SELECT s.Answer FROM s3object s WHERE Category = 'TREASURE'" --expression-type sql --input-serialization '{"CSV": {"FileHeaderInfo": "USE", "FieldDelimiter": ";"}, "CompressionType": "GZIP"}' --output-serialization '{"CSV": {}}' --profile tmp treasure6


I'm also analyzed s3select.csv.gz by Excel