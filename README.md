# Azure Policy: Tags

Apply tags on resources and resource groups in order to identify the owner and needs of this resources and calculate the cost by departments.

Let's assume we want to enforce each resource or resource group a tag of environment with a value of prod/dev/qa. We will apply a policy to require this Tag and check the value is one of the allowed values.

בנוסף, יש כמה עניינים נוספים בהגדרת תגים

Due to a thecnical reason, Azure require seperating tag policies of Resources from tag policies of resource groups.

כדי שנוכל להציג למשתמש הודעות מסודרות על הסיבה המדויקת לבעיה, כדי להפריד את החוקים לבדיקות אטומיות ככל שאפשר

In order to make it easier for users to set the tags, we want to automatically copy the tag and value from the resource group to the resources.

The following policies will need to apply for this matter:
1. Require the tag on Resource Groups
2. Require the tag on Resources
3. Check the value is one of the allowed value on Resource Groups
4. The same of (3) on other resources
5. Append the Tag and Value from the resource group

Our best practicies 

Due to a thecnical reason, Azure require seperating tag policies of Resources from tag policies of resource groups. We will need to create 2 polici

Instead of creating lot of policy assignment for each of our 

The following table describe sample Tags and with settings according the organization need:

|Tags name     |Required |Values   |Target |description|
|--------------|---------|---------|-------|-----------|
|Cost center   |Yes	     |L2A, Hub |Resource Group	|Contains the project name or system name
|Business owner|Yes		   |         |Resource Group	|Contains the business owner of the cost center app/project
|Infra owner   |Yes	     | EAI, DB, EMS	| Resource Group|Contains the infra owner of the cost center app/project
|Environment   |Yes	     | Prod, Dev, Test, SBOX |Resource Group|Represents the environment


