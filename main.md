```bash
    provider "aws" {
        region = "us-east-1"
    }
```

```bash
    resource "aws_vpc" "main" {
        cidr_block = "10.5.0.0/16"

        tags = {
            "Name" = "Private VPC"
        }
    }
```

```bash
    resource "aws_subnet" "public_subnet" {
        vpc_id = aws_vpc.main.id
        cidr_block = "10.5.0.0/16"

        tags = {
            "Name" = "Private VPC"
        }
    }
```

```bash
    resource "aws_instance" "ubuntu_server" {
        ami = "your AMI"
        instance_type = "t2.micro"
        subnet_id = aws_subnet.public_subnet.id

        tags = {
            "Name" = "My Ubuntu Server"
        }

    }
```