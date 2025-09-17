Parameters: 

to provide inputs to CloudFormation Template
they are important if we want to reuse
parameters are extremely powerful
parameters are CROSS-Validated using Rules
To reference a parameter we use::Ref
shorthand for this YAML is !Ref
!Ref function works well with referencing to the parameters as well as templates within resources in CF template


Resources:

core of CF Templates
Mandatory
over 700 types of resources
Resource types identifiers are of form:
     AWS::aws-product-name::data-type-name




Treat AWS Architecture like source code - any changes to template - another version
    - Create Stack of resources - can estimate costs

Templates & Stacks
    - Template is either JSON or YAML formatted text
    - Blueprint
    - Stack is comprised of resources created by CloudFormation
    - Resources in stack  - tagged to identifier - stack costs
    
Change set --> for template 1 and template 2