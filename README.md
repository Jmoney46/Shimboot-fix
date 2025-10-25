# Shimboot-fix
Goes over a problem I ran into when setting up shimboot on chromebook regaurding "cros_debug" when using the premade shims we was provided with.

# Method 1: How to make one yourself adding cros_debug (most do able)
So basically when you are making the shimboot like normal 
1.) build_image --board $BOARD, this is what it looks like normally, this is not what you want because it can get pretty gay.
2.) now, before you enter add "--boot_args cros_debug factory_install", this is what adds cros_debug to your sh1t.
3.) or you can just copy the code I put in the file.
