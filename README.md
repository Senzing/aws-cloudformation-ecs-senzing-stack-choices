# aws-cloudformation-ecs-senzing-stack-choices

## Synopsis

The `aws-cloudformation-ecs-senzing-stack-choices` AWS Cloudformation template
deploys user-specified components of the Senzing stack for use with a previously deployed
[aws-cloudformation-database-cluster](https://github.com/Senzing/aws-cloudformation-database-cluster) Cloudformation stack
that has been initialized by deploying the
[aws-cloudformation-ecs-senzing-stack-basic](https://github.com/Senzing/aws-cloudformation-ecs-senzing-stack-basic) Cloudformation stack.

## How to deploy

1. :warning: **Warning:** This Cloudformation deployment will accrue AWS costs.
   With appropriate permissions, the
   [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/)
   can help evaluate costs.
1. Download the appropriate [AWS Cloudformation template example](https://raw.githubusercontent.com/Senzing/aws-cloudformation-ecs-senzing-stack-choices/main/cloudformation.yaml) from this repository to your local device.  Example:
    ```
    curl -X GET \
        --output ~/cloudformation.yaml \
        https://raw.githubusercontent.com/Senzing/aws-cloudformation-ecs-senzing-stack-choices/main/cloudformation.yaml
    ```
3. It is highly suggested to take a look at the AWS Cloudformation Template that has been downloaded.  This template is an example that deploys and configures a number of services and facilities.  While it is a working and complete example, each business may have different requirements and their account may not have all the privledges required to deploy it.  Furthermore, the examples change over time and these files are meant to be treated as code files so they should be put under source control.
1. Visit the [AWS Cloudformation home](https://console.aws.amazon.com/cloudformation/home).
1. At the upper-right, click the "Create stack" drop-down and choose "With new resources (standard)".
1. In the "Specify template" area choose the "Upload a template file" radio button.
1. Select the "Choose file" button and choose the AWS Cloudformation template that was downloaded previously.
1. At lower-right, click on "Next" button.
1. In **Specify stack details**
    1. In **Stack name**
        1. Choose a stack name that is unique to you and 21 characters or less.  (Several resource types have a limit of 32 character names. The CFT uses the stack name and an 11 character suffix to name resources uniquely.)
    1. In **Parameters**
        1. In **Senzing installation**
            1. Accept the End User License Agreement.
            1. Optionally, choose a version of Senzing to install.
            1. Optionally, add a license string.
        1. In **Identify existing resources**
            1. Enter the stack name of the previously deployed
               [aws-cloudformation-database-cluster](https://github.com/Senzing/aws-cloudformation-database-cluster)
               Cloudformation stack
               Example:  `senzing-db`
        1. In **Security**
            1. Provide the email address for the administrative user.  Example: `me@example.com`
            1. Provide the permitted IP address block allowed to connect using CIDR notation.  Note: to open the installation to any IP address use: `0.0.0.0/0`.  For more on CIDR, see [Classless Inter-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)
        1. In **Optional: Initial data load**
            1. If loading data during deployment is desired, choose "Yes" for *"Optional: Would you like to have an initial set of data imported?"*
            1. If "Yes" is chosen, the other field specify what data is to be loaded.
        1. In **Optional: Service**
            1. Individual services can be selected.
        1. In **Security responsibility**
            1. Understand the nature of the security in the deployment.
            1. Once understood, enter "I AGREE".
    1. At lower-right, click "Next" button.
1. In **Configure stack options**
    1. At lower-right, click "Next" button.
1. In **Review senzing-basic**
    1. Near the bottom, in **Capabilities**
        1. Check ":ballot_box_with_check: I acknowledge that AWS CloudFormation might create IAM resources."
    1. At lower-right, click "Create stack" button.

## Additional topics

1. [Details of deployment](docs/README.md)
1. [How to load AWS Cloudformation queue](https://github.com/Senzing/knowledge-base/blob/main/HOWTO/load-aws-cloudformation-queue.md)
1. [How to update Senzing license](https://github.com/Senzing/knowledge-base/blob/main/HOWTO/update-senzing-license.md)
