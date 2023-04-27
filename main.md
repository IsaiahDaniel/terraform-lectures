```bash
provider "aws" {
  region = "us-east-1"
}

```

```bash

locals {
  prefix = "QOMPLX-"
}

```

```bash

resource "aws_instance" "ubuntu_server_1" {
  ami = "ami-007855ac798b5175e"
  instance_type = "t2.micro"

  tags = {
    "Name" = "${local.prefix}UbuntuServer 1"
  }

}

```

```bash

resource "aws_instance" "ubuntu_server_2" {
  ami = "ami-007855ac798b5175e"
  instance_type = "t2.micro"

  tags = {
    "Name" = "${local.prefix}UbuntuServer 2"
  }

}

```

```bash
resource "aws_instance" "ubuntu_server_3" {
  ami = "ami-007855ac798b5175e"
  instance_type = "t2.micro"

  tags = {
    "Name" = "${local.prefix}UbuntuServer 3"
  }

}

```