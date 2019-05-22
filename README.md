# Hands-On Infrastructure Automation with Terraform on AWS

## HCL - Hashicorp Configuration Language

Terraform configurations are written in HCL. HCL means Hashicorp Configuration Language and
was created targeting be an human-friendly configuration language.

### HCL Syntax

#### 1. Single Line Comment

```hcl
// Single comment
```

#### 2. Hash Comment

```hcl
# Hash comment
```

#### 3. Multi-Line Comment

```hcl
/*
  Multi-line
  comment example
*/
```

#### 4. Variables

```hcl
variable "ami" {
  description = "Some AMI"
}

variable "zones" {
  type    = "list"
  default = ["us-east-1a", "us-east-1b"]
}
```

#### 5. Resource

```h
resource "aws_resource_type" "xpto" {
  string_attribute = "${var.ami}"
  integer_attribute = 2
  boolean_data = false
  text_data = <<EOF
#!/bin/bash
echo "Terraform rocks"
EOF
}
```
