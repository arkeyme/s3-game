    aws s3 cp s3://s3game-level6-vjv45x1gux81 ./ --recursive --profile s3-game
    aws s3api list-objects --bucket s3game-level6-vjv45x1gux81 --profile s3-game

    aws s3api select-object-content --bucket s3game-level6-vjv45x1gux81 --key s3select.csv.gz --expression "SELECT s.Answer FROM s3object s WHERE Category = 'TREASURE'" --expression-type sql --input-serialization '{"CSV": {"FileHeaderInfo": "USE", "FieldDelimiter": ";"}, "CompressionType": "GZIP"}' --output-serialization '{"CSV": {}}' --profile s3-game treasure6


I'm also analyzed s3select.csv.gz by Excel