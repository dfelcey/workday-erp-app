# Overview
This Workday ERP application provides operations for creating or updating Contacts using the [Workday Revenue Management Module](https://community.workday.com/sites/default/files/file-hosting/productionapi/Revenue_Management/v33.0/Revenue_Management.html) The Id of the Workday Contact should correspond to the name Business Entity that the Contact that is associated with.

## Contact *Upsert*
If a Contact already exists then it will be updated. Otherwise a new contact will be created. Dates must be in the format `2015-07-04T21:00:00` and the delete operation is currently a *no-op* operation

# Configuration
Before deploying the application it needs to be configured with the correct Workday connection parameters. These are set in the 3 configuration files in the dire src/main/resources These  have the name `<env>-config.properties`, where `<env>` is the environment the application is deployed to (`dev`, `test` or `prod`).

The environment parameter that determines which configuration file is used is set using a system property, `mule.env`, that can be set at runtime. The default environment is `test`

# Additional Notes
To run this application the user needs to have the appropriate permissions 