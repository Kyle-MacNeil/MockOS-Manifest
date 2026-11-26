# Yocto Build Environment Setup

To build the Yocto Build Environment, enter the following command lines in your Linux system:
	
	mkdir yocto-workspace
	
	cd yocto-workspace
	
	repo init -u <MANIFEST_REPO_URL> -b <branch>
		*Replace <branch> with your desired BSP branch*
		*Replace <MANIFEST_REPO_URL> with the URL of your manifest repository*
		
	repo sync
	
	source <setup-script>
		*Replace <setup-script> with your environment setup script (e.g., setupsdk or oe-init-build-env)*
	
After these command lines, you should have the build environment completely built and are ready to start building images.

## Building the Image

To build the BSP image, enter the following:

	cd /<path-to-workspace>/yocto-workspace
	
	bitbake <target-image-name>
		*Replace <target-image-name> with your desired image recipe (e.g., core-image-minimal or petalinux-image-minimal)*