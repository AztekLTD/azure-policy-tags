# Azure Policy: Tags

Apply tags on resources and resource groups in order to identify the owner and needs of this resources and calculate the cost by departments.
The following table describe sample Tags and with settings according the organization need:

|Tags name     |Required |Values   |Target |description|
|--------------|---------|---------|-------|-----------|
|Cost center   |Yes	     |L2A, Hub |Resource Group	|Contains the project name or system name
|Business owner|Yes		   |         |Resource Group	|Contains the business owner of the cost center app/project
|Infra owner   |Yes	     | EAI, DB, EMS	| Resource Group|Contains the infra owner of the cost center app/project
|Environment   |Yes	     | Prod, Dev, Test, SBOX |Resource Group|Represents the environment
