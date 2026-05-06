*S3*
Bronze Bucket Name = youtube-data-pipeline-bronze-us-east-1-aws
Silver Bucket Name = youtube-data-pipeline-silver-us-east-1-aws
Gold Bucket Name = youtube-data-pipeline-gold-us-east-1-aws
Scripts Bucket Name = youtube-data-pipeline-script-us-east-1-aws
Athena Query Results = yt-data-pipeline-glue-athena-query-result-aws

*Simple Notification Service - SNS*
SNS ARN = arn:aws:sns:us-east-1:628165508199:yt-data-pipeline-alerts-dev:2915991b-1b9f-4e1b-8787-c3df9dd67ddf

*Glue*
**Databases**
Glue Bronze = yt_pipeline_bronze_dev
Glue Silver = yt_pipeline_silver_dev
Glue Gold = yt_pipeline_gold_dev
**ETL Jobs**
yt-data-pipeline-silver-to-gold-dev
yt-data-pipeline-bronze-to-silver-dev
**Crawlers**
yt-data-pipeline-bronze-crawler-dev

*Identity and Access Management - IAM*
**Roles**
yt-data-pipeline-glue-role-dev
yt-data-pipeline-lambda-role-dev
yt-data-pipeline-stepfunction-role-dev

*Lambda*
**Functions**
yt-data-pipeline-data-quality-dev
yt-data-pipeline-youtube-ingestion-dev
yt-data-pipeline-json-to-parquet-dev




--bronze_database yt_pipeline_bronze_dev
--bronze_table raw_statistics
--silver_bucket youtube-data-pipeline-silver-us-east-1-aws
--silver_database yt_pipeline_silver_dev
--silver_table clean_statistics

--silver_database yt_pipeline_silver_dev
--gold_bucket youtube-data-pipeline-gold-us-east-1-aws
--gold_database yt_pipeline_gold_dev