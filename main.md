```bash
    provider "aws" {
        region = "us-east-1"
    }
```

```bash
    resource "aws_instance" "ubuntu_server" {
        ami = "your AMI"
        instance_type = "t2.micro"

        tags = {
            "Name" = "My Ubuntu Server"
        }

    }
```