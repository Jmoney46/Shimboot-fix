# Shimboot-fix
Goes over a problem I ran into when setting up shimboot on chromebook regaurding "cros_debug" when using the premade shims we was provided with.

<br>IMPORTANT! SHIMBOOT REQUIRES "Firmware utility script" WHICH YOU MUST GET FROM https://docs.mrchromebox.tech/docs/fwscript.html<br>

# Method 1: How to make one yourself adding cros_debug (most do able)
So basically when you are making the shimboot like normal 
<br>1.) build_image --board $BOARD, this is what it looks like normally, this is not what you want because it can get pretty gay.<br>
<br>2.) now, before you enter add "--boot_args cros_debug factory_install", this is what adds cros_debug to your sh1t.<br>
<br>3.) or you can just copy the code I put in the file.<br>

# Method 2: Add it to an already existing one (requires dev mode enabled)
Add it to one of the ones you are provided with, (or you have already made)
<br>1.) For an existing image you will need "make_dev_ssd.sh" added to the command line (available at chromeos chroot by ~/trunk/src/platform/vboot_reference/scripts/image_signing/make_dev_ssd.sh)<br>
<br>2.) "./make_dev_ssd.sh -i $PATH_TO_IMAGE_OR_USB_DEVICE --partitions 2 --recovery --edit_config", by adding this it will open a editor that allows you to add cros_debug<br>
