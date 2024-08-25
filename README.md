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
I am here to tell you about how to build a nethunter from scratch. What we need is a custom made kernel so that we can have a full access to the hardware of the device. 


## Building a kernel

1. Find the kernel source, this is something which needs to be released by the manufacturer, ex for samsung devices you can find it at https://developer.samsung.com/ . If you are using a custom rom which is recommended then you will mostly likely find a github link to the kernel source on its xda page, or else just ask the dev who build the ROM.
2. With the kernel source there will be instructions given about how to build the kernel, go to the MAKE menu and the config in [this file](./assets/config)

![Nethunter kernel](https://www.kali.org/docs/nethunter/nethunter-kernel-2-config-1/nh-kernel-120-modules.png)

If you face any issue then you might have to use some patches which are available [here](https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-kernel).
3. Using [Anykernel](https://github.com/osm0sis/AnyKernel3) by Osmosis to flash the compiled image, you can also directly flash the image but here you will always need a pc in hand.
4. Preparing the Device: Install a custom rom, root the device using magisk.
5. Flash the Kernel 
6. Install nethunter arm through magisk.

Voila Done.


![My Image](./assets/b.jpeg)

Shitty note: I know you might get many many errors if you are newbie, but their is a huch community support available on telegram about building kernels so please join there.

