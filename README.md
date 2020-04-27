# apisec-cli
### Copyright (c) apisec.ai inc.
### https://www.apisec.ai


## Getting Started

To download and run apisec-cli, please run the following
```sh
git clone https://github.com/intesar/apisec-cli
cd apisec-cli
java -jar apisec-cli.jar
```

## Sign-up Command
When you sign-up a new organization account will be created in the apisec cloud platform.
```sh
apisec> signup –c <company> -e <email>
```

## Login Command
```sh
apisec> login –u <email> -p <password>
```

## API Register Command
Register one more more APIs.
```sh
apisec> register -n <api-name> -o <OpenAPI Specification URL>
```

## List APIs Command
Lists registered APIs
```sh
apisec> ls
```


## Scan Command
Fire a security scan
```sh
apisec> scan -n <api-name>
```


## Deploy Local Scanners
Run a scanner on Docker or Kubernetes host and scan APIs running in local or in private enviornment. 
```sh
apisec> scanner create -n <scanner-name>
```

Now use the local scanner to fire the scan.
```sh
apisec> scan –n <api-name> –s <scanner-name>
```

## List Scanners
```sh
apisec> scanner ls
```

## Delete Scanners
Delete registered scanner in the apisec cloud environment. Make sure to delete the scanner from the Docker and Kubernetes host.
```sh
apisec> scanner rm -n <scanner-name>
```
