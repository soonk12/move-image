References
- https://docs.aws.amazon.com/lambda/latest/dg/with-s3-example.html
- https://caolan.github.io/async/docs.html#waterfall
- https://www.regexpal.com/
-


Commands:

Zip new version of function
zip -r function.zip .

Upload changed code:
aws --region us-east-2 lambda update-function-code --function-name MoveImage --zip-file fileb://function.zip

Invoke test function:
aws --region us-east-2 lambda invoke --function-name MoveImage --invocation-type Event --payload file://inputfile.txt outputfile.txt
