# Running Map Reduce Jon in AWS EMR

## Step-1
aws emr put --cluster-id j-3TXOQESQSYTA2	 --key-pair-file "javahome.pem" --src "/Users/kammana/java/emr-app/target/samples-1.0.0.jar"

## Step-2
aws emr ssh --cluster-id j-3TXOQESQSYTA2	 --key-pair-file "javahome.pem" --command "hadoop jar samples-1.0.0.jar com.amazonaws.samples.WordCountJobConfig s3://javahome-emr-wordcount/input/words.txt  s3://javahome-emr-wordcount/output/1"
