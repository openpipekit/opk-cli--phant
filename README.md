
A commandline client for pushing data to the Open Source Phant data service. 

# Requirements
- Node.js

# Usage

Set up a stream on something like http://data.sparkfun.com and then run...
```
./push
  --url <url> Example: data.sparkfun.com
  --public_key <public_key> Example: RM1nQNbVRGtaMMgvVz8Y
  --private_key <private_key> Example: lz6d0j7KxPH1VVryqMw5
  --field_name <field_name> Example: temp
  --data [data] This is optional because you can also pipe data to this command.
  --stream Accept streaming piped data, i.e. dosomething.sh | ./push --stream
  --json Accept json data, i.e. {first:1,second:2}

Example: ./push --verbose --url data.sparkfun.com --public_key lzELagraWDiMMRra0V6Q --private_key XXXXXXXXXX --field_name temp
```


