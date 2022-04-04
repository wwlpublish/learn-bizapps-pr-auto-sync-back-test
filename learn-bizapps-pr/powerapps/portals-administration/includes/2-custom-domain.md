When a portal is provisioned, it will have a portal URL that is a subdomain of `powerappsportals.com`, for example, `contoso.powerappsportals.com`. A common task for a portal administrator is to configure a custom URL for a Power Apps portal to reflect the domain naming conventions of an organization such as `https://www.contoso.com`.  

> [!NOTE]
> You can have only one custom URL for each portal.

## Add a custom URL to a Power Apps portal

The following sections describe how to add a custom URL to a Power Apps portal.

### Prerequisites

The organization needs to own the specific domain name and have a valid SSL certificate for the domain. The administrator also needs to have access to configure DNS settings for the custom URL.

Additionally, the portal cannot be in **Trial** mode when you are adding a custom domain.

### Install the SSL certificate

In the Power Apps portals admin center, the **Manage SSL certificates** section will be where an SSL certificate will be uploaded.

The SSL certificate will require a PFX file extension and it must meet the following requirements:

- Signed by a trusted certificate authority
- Exported as a password-protected PFX file
- Contains a private key that is at least 2048 bits long
- Contains all intermediate certificates in the certificate chain
- SHA2 enabled (SHA1 support is being removed from popular browsers)
- PFX file must be encrypted with TripleDES encryption; Power Apps portals doesn't support AES-256 encryption

The specific domain name will need to have a CNAME record that is set up in DNS to point to the `contoso.powerappsportals.com` domain that was configured during the portal provisioning process.

The final step is to bind the custom domain and the SSL certificate. Visitors should now be able to browse to the portal by using the custom URL.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Add SSL binding window.](../media/binding.png)](../media/binding.png#lightbox)

> [!NOTE]
> If you want to change your existing custom domain name, upload a new SSL certificate and follow the preceding steps.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4AwWW]

For more information, see [Add a custom domain](/power-apps/maker/portals/admin/add-custom-domain/?azure-portal=true).
