```bash 
variable "instance_type" {
  default = "t2.micro"
  type = string
  description = "Holds instance type"
}

```

```bash
resource "aws_instance" "ubuntu_server" {
  ami = "ami-007855ac798b5175e"
  instance_type = var.instance_type
  # subnet_id = aws_subnet.public_subnet.id

  tags = {
    "Name" = "Ubuntu Server"
  }

}
```

```bash
resource "aws_instance" "ubuntu_server2" {
  ami = "ami-007855ac798b5175e"
  instance_type = var.instance_type
  # subnet_id = aws_subnet.public_subnet.id

  tags = {
    "Name" = "Ubuntu Server 2"
  }

}

```