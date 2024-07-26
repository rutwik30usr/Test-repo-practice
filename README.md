# Test-repo-practice

resource "aws_security_group" "allow_tls" {
  name        = "allow_tls"
  description = "Allow TLS inbound traffic and all outbound traffic"

  ingress {
    description = "TLC from VPC"
    from_port = "3389"
    to_port = "3389"
    protocol = "tcp"
    cidr_blocks = [ "0.0.0.0/0" ]
  }
