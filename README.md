# TowardsNethunter



## What is Kali Nethunter? 🤔
Kali NetHunter is an open-source mobile penetration testing platform developed by Offensive Security. It is essentially a mobile version of Kali Linux, a popular Linux distribution used by cybersecurity professionals for penetration testing, ethical hacking, and digital forensics.

![My Image](./assets/a.jpeg)

## Why Nethunter though?
Imagine carrying the full power of a world-class penetration testing environment not in a bulky laptop bag, but right in your pocket. That’s the Kali NetHunter—a portable, flexible, and dynamic version of Kali Linux tailored for the mobile world. But why should you choose NetHunter over the traditional Kali setup? Let’s dive into the reasons, and you might just find yourself inspired to go mobile.

![Nethunter App](https://www.kali.org/docs/nethunter/NetHunter-App.png)


### The Final Word: A New Era of Pentesting
Choosing Kali NetHunter over regular Kali isn’t just about opting for mobility; it’s about embracing a new era of penetration testing. It’s about understanding that in today’s fast-paced world, the ability to adapt and respond on the fly is more critical than ever. With NetHunter, you’re not just carrying a toolkit—you’re carrying the future of cybersecurity in your pocket.

So, why stick to the old ways when you can redefine your approach? Kali NetHunter is more than just an alternative; it’s an evolution. It’s time to unleash the power of mobile pentesting and see where it takes you

## Toolset and Capabilities:

NetHunter comes pre-installed with a comprehensive suite of tools found in Kali Linux, tailored for mobile use. This includes tools for network scanning, Wi-Fi cracking, web application testing, and more.
Unique mobile-specific tools are also available, such as HID (Human Interface Device) keyboard attacks, BadUSB attacks, and Wi-Fi frame injection, which are particularly useful for conducting physical penetration tests.

## Integration into Android:

Kali NetHunter is a custom Android ROM overlay that can be installed on a range of Android devices. It integrates with the Android OS, enabling users to leverage the full power of their mobile device for penetration testing tasks.
While some features require root access, NetHunter can also be installed on unrooted devices, offering a flexible setup depending on the user's needs.

## Getting started with kali nethunter

Finally its time to begin the Journey. Here are the [Documentation](https://www.kali.org/docs/nethunter/) for the official Devices.

# But what about unsupported devices?
I am here to tell you about how to build a nethunter from scratch. What we neeed is a custom made kernel so that we can have a full access to the hardware of the device. 


## Building a kernel

1. Find the kernel source, this is something which needs to be released by the manufacturer, ex for samsung devices you can find it at https://developer.samsung.com/ . If you are using a custom rom which is recommended then you will mostly likely find a github link to the kernel source on its xda page, or else just ask the dev who build the ROM.
2. With the kernel source there will be instructions given about how to build the kernel, go to the MAKE menu and then select the following things.
![Nethunter kernel](https://www.kali.org/docs/nethunter/NetHunter-App.png](https://www.kali.org/docs/nethunter/nethunter-kernel-2-config-1/nh-kernel-120-modules.png)


CONFIG_SYSVIPC=y
CONFIG_SYSVIPC_SYSCTL=y
CONFIG_SYSVIPC_COMPAT=y
CONFIG_SYSTEM_DATA_VERIFICATION=y
CONFIG_MODULE_FORCE_LOAD=y
CONFIG_MODULE_SIG=y
CONFIG_MODULE_FORCE_UNLOAD=y
CONFIG_MODULE_SIG_ALL=y
CONFIG_MODULE_SIG_SHA1=y
CONFIG_MODULE_SIG_HASH="sha1"
CONFIG_PKCS7_MESSAGE_PARSER=y
CONFIG_MODULE_SIG_KEY="certs/signing_key.pem"
CONFIG_SYSTEM_TRUSTED_KEYRING=y
CONFIG_WLAN_VENDOR_MEDIATEK=y
CONFIG_ANDROID_BINDER_IPC=y
CONFIG_WANT_DEV_COREDUMP=y
CONFIG_DEV_COREDUMP=y
CONFIG_USB_NET_RNDIS_HOST=y
CONFIG_WLAN_VENDOR_ADMTEK=y
CONFIG_ATH_COMMON=y
CONFIG_ATH9K_HW=y
CONFIG_ATH9K_COMMON=y
CONFIG_ATH9K_BTCOEX_SUPPORT=y
CONFIG_ATH9K=y
CONFIG_ATH9K_PCOEM=y
CONFIG_ATH9K_HTC=y
CONFIG_RT2X00=y
CONFIG_RT2500USB=y
CONFIG_RT73USB=y
CONFIG_RT2800USB=y
CONFIG_RT2800USB_RT33XX=y
CONFIG_RT2800USB_RT35XX=y
CONFIG_RT2800USB_RT3573=y
CONFIG_RT2800USB_RT53XX=y
CONFIG_RT2800USB_RT55XX=y
CONFIG_RT2800USB_UNKNOWN=y
CONFIG_RT2800_LIB=y
CONFIG_RT2X00_LIB_USB=y
CONFIG_RT2X00_LIB=y
CONFIG_RT2X00_LIB_FIRMWARE=y
CONFIG_RT2X00_LIB_CRYPTO=y
CONFIG_RT2X00_LIB_LEDS=y
CONFIG_RTL8187=y
CONFIG_RTL8187_LEDS=y
CONFIG_RTL_CARDS=y
CONFIG_RTL8192CU=y
CONFIG_RTLWIFI=y
CONFIG_RTLWIFI_USB=y
CONFIG_RTLWIFI_DEBUG=y
CONFIG_RTL8192C_COMMON=y
CONFIG_RTL8XXXU=y
CONFIG_RTL8XXXU_UNTESTED=y
CONFIG_88XXAU=y
CONFIG_WLAN_VENDOR_ZYDAS=y
CONFIG_USB_ZD1201=y
CONFIG_USB_NET_RNDIS_WLAN=y
CONFIG_CRYPTO_KPP=y
CONFIG_CRYPTO_ECDH=y
CONFIG_CRYPTO_CCM=y
CONFIG_CRYPTO_CMAC=y
CONFIG_CRC_ITU_T=y
CONFIG_USB_ACM=y
CONFIG_USB_OTG=y
CONFIG_HID=y
CONFIG_HIDRAW=y
CONFIG_UHID=y
CONFIG_HID_GENERIC=y
CONFIG_USB_CONFIGFS_SERIAL=y
CONFIG_USB_CONFIGFS_ACM=y
CONFIG_USB_CONFIGFS_OBEX=y
CONFIG_USB_CONFIGFS_NCM=y
CONFIG_USB_CONFIGFS_ECM=y
CONFIG_USB_CONFIGFS_ECM_SUBSET=y
CONFIG_USB_CONFIGFS_RNDIS=y
CONFIG_USB_CONFIGFS_EEM=y
CONFIG_USB_CONFIGFS_MASS_STORAGE=y
CONFIG_USB_CONFIGFS_F_HID=y
CONFIG_USB_HID=y
CONFIG_USB_HIDDEV=y
CONFIG_USB_F_ACM=y
CONFIG_USB_U_SERIAL=y
CONFIG_USB_U_ETHER=y
CONFIG_USB_F_SERIAL=y
CONFIG_USB_F_OBEX=y
CONFIG_USB_F_NCM=y
CONFIG_USB_F_ECM=y
CONFIG_USB_F_EEM=y
CONFIG_USB_F_SUBSET=y
CONFIG_USB_F_RNDIS=y
CONFIG_USB_F_MASS_STORAGE=y
CONFIG_USB_F_FS=y
CONFIG_USB_F_UVC=y
CONFIG_USB_HID=y
CONFIG_USB_ANNOUNCE_NEW_DEVICES=y
CONFIG_USB_F_HID=y
CONFIG_USB_F_MTP=y
CONFIG_USB_CONFIGFS=y
CONFIG_USB_CONFIGFS_SERIAL=y
CONFIG_USB_CONFIGFS_ACM=y
CONFIG_USB_CONFIGFS_OBEX=y
CONFIG_USB_CONFIGFS_NCM=y
CONFIG_USB_CONFIGFS_ECM=y
CONFIG_USB_CONFIGFS_ECM_SUBSET=y
CONFIG_USB_CONFIGFS_RNDIS=y
CONFIG_USB_CONFIGFS_EEM=y
CONFIG_USB_CONFIGFS_MASS_STORAGE=y
CONFIG_USB_CONFIGFS_F_MTP=y
CONFIG_USB_RNDIS_MULTIPACKET=y
CONFIG_USB_CONFIGFS_F_MIDI=y
CONFIG_USB_CONFIGFS_F_HID=y
CONFIG_USB_F_ACM=y
CONFIG_USB_U_SERIAL=y
CONFIG_USB_U_ETHER=y
CONFIG_USB_F_SERIAL=y
CONFIG_USB_F_OBEX=y
CONFIG_USB_F_NCM=y
CONFIG_USB_F_ECM=y
CONFIG_USB_F_EEM=y
CONFIG_USB_F_SUBSET=y
CONFIG_USB_F_RNDIS=y
CONFIG_USB_F_MASS_STORAGE=y
CONFIG_USB_F_MIDI=y

If you face any issue then you might have to use some patches which are available [here](https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-kernel).
3. Using [Anykernel](https://github.com/osm0sis/AnyKernel3) by Osmosis to flash the compiled image, you can also directly flash the image but here you will always need a pc in hand.
4. Preparing the Device: Install a custom rom, root the device using magisk.
5. Flash the Kernel 
6. Install nethunter arm through magisk.

Voila Done.

Shitty note: I know you might get many many errors if you are newbie, 

