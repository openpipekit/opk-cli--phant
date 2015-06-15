# OPK Phant CLI
A commandline client for pushing data to the Open Source Phant data service. 

```
./push
  --url <url> Example: data.sparkfun.com
  --public_key <public_key> Example: RM1nQNbVRGtaMMgvVz8Y
  --private_key <private_key> Example: lz6d0j7KxPH1VVryqMw5
  --field_name <field_name> Example: temp
  --data [data] This is optional because you can also pipe data to this command.
  --stream Accept streaming piped data, i.e. dosomething.sh | ./push --stream
  --json Accept json data, i.e. {first:1,second:2}
```

## Requirements
- Node.js

## Usage
Set up a stream on something like http://data.sparkfun.com and then run...
```
echo "42" | ./opk-phant-cli/push --url data.sparkfun.com --public_key XXXXXXXXXX --private_key XXXXXXXXXX --field_name yourfieldname
```
You can also send structured data without having to define just one `field_name` parameter by doing...
```
echo '{"temperature": 42, "humidity": .3}' | ./opk-phant-cli/push --url data.sparkfun.com --public_key XXXXXXXXXX --private_key XXXXXXXXXX
```
If the CLI that pipes data to the phant cli streams data as opposed to giving one value and exiting, use the stream flag in the command.
```
./opk-somedriver-cli/pull | ./opk-phant-cli/push --stream --url data.sparkfun.com --public_key XXXXXXXXXX --private_key XXXXXXXXXX
```







