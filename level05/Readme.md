    aws s3api list-object-versions --bucket s3game-level5-8v95e5rv7z4i --profile s3-game > obj_versions

At first I tried to get object by version id of delete marker, but it does not work, so I retrieved version by version-id of original object. 

    aws s3api get-object --bucket 's3game-level5-8v95e5rv7z4i' --key treasure5_is_deleted --version-id '344PQOyFqocF0TI66MbLynNNdQqHfBz3' --profile s3-game treasure5_is_deleted

