This script uses Git to back up files to cloud code hosting platforms. All files are encrypted using a public GPG key. Since encryption requires only the public key, this script is ideal for running on home NAS devices—the private key needed for decryption stays in a secure location (hopefully yours). For example, i am using Ybikey 5 for GPG storage. You can access your backed-up files without entering credentials for the code hosting service, which offers added convenience.

By default, the script backs up files daily at 08:55. 

Setup requires:

- Generate GPG and SSH key pairs. GPG encrypts/decrypts data; SSH enables secure pulling from your code host.
- Clone the repository to your user's home directory root.
- Initialize the repository in the repo folder and connect it to your code hosting service.
- Update environment variables in the script to match your setup. Since this script was written for my specific use case, you may need to adjust more than just the variables.
- Copy the systemd service and timer unit files to the appropriate location.
- Modify the service file if necessary.
- Test the service, and if it works correctly, enable and start the timer.
