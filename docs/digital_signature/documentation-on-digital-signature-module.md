# Digital Signature in OS2forms

Link to module: https://github.com/OS2Forms/os2forms/modules/os2forms_digital_signature/
JIRA case: https://os2web.atlassian.net/browse/S2FRMS-57

In order to digitally sign a document in OS2forms, the “OS2Forms Digital Signature” module must be installed and configured.

The installation takes place under “Extend” and after installation, the configuration can be found via “Settings” \-\> “System” \-\> “OS2Forms Digital Signature”.

There are 4 values ​​that must be configured in order to use digital signature.

* **Signature server URL:** The URL of the service providing digital signature. This is an example of a known service: https://signering.bellcom.dk/sign.php?  
* **Hash Salt used for signature:** Must match the Hash Salt on the signature server.  
* **List IP's which can download unsigned PDF submissions:** Here, IP addresses that should be able to download the unsigned PDF file that the submission has generated can be entered. This will typically be the IP address of the signature server, which should be able to retrieve the PDF file in order to sign it.  
* **Unsigned submission timespan(s):** This specifies the number of seconds that must pass from the time the unsigned submission is made until it must be signed. If this number of seconds is exceeded, the unsigned submission will be automatically deleted.

Once this configuration has been made, the module is ready for use.

## How to use Digital Signature in OS2forms?

You create your form as usual, with the elements you want in the form.

The digital signature is made via “The Danish Digital Agency's signing component” (in danish: “Digitaliseringsstyrelsens signeringskomponent”), which shows the signer a PDF file, which the signer then signs. Therefore, it requires that you have the element “OS2Forms Attachment” added to your form, as that element can generate a PDF file.

When the module “OS2Forms Digital Signature” is installed, there is an option to turn “Digital signature” on and off under “Attachment settings” on the element “OS2Forms Attachment”. If you enable it, the PDF file that the element generates when submitted will be sent for signing.

In addition to enabling “Digital signature” on the “OS2Forms Attachment” element, the “Digital Signature” handler must also be added. Do this under “Settings” \-\> “Emails / Handlers” \-\> “+ Add handler”. No setup/configuration is required for the “Digital Signature” handler.

If you have some email handlers on your form and you would like to wait for them to be sent until the digital signature has taken place, you must go into each of these handlers and set them to only be sent when the submission is locked.

This is done under “Advanced” and under “Additional settings”, where you can check the box under “…when submission is locked.”

## What is not supported in the PDF file for digital signing?

* We currently know that “The Danish Digital Agency's signing component” (in danish: “Digitaliseringsstyrelsens signeringskomponent”) does not support the way Drupal creates links in PDF files. This applies to both the elements in the PDF file, but also the header, footer and colophon.