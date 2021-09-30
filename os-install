## Hardware requirements

### You will need:
#### 1) high spec laptop e.g. recent Intel Core i7 with 16GB of RAM
#### 2) blank USB stick 8GB or larger (for installation)

Qubes OS has very specific [system requirements](https://www.qubes-os.org/doc/system-requirements/). To
ensure compatibility:

* ask Iguana

* check this document for hardware Jungle members have personally tested / recommended

* consult the [Hardware Compatibility List](https://www.qubes-os.org/hcl/)

Even on supported hardware, you must ensure that [IOMMU-based
virtualization](https://en.wikipedia.org/wiki/Input%E2%80%93output_memory_management_unit#Virtualization)
is activated in the BIOS or UEFI. Without it, Qubes OS won't be able to enforce
isolation. For Intel-based boards, this setting is called Intel Virtualization
for Directed I/O (**Intel VT-d**) and for AMD-based boards, it is called  AMD
I/O Virtualization Technology (or simply **AMD-Vi**). This parameter should be
activated in your computer's BIOS or UEFI, alongside the standard
Virtualization (**Intel VT-x**) and AMD Virtualization (**AMD-V**) extensions.
This [external
guide](https://web.archive.org/web/20200112220913/https://www.intel.in/content/www/in/en/support/articles/000007139/server-products.html)
made for Intel-based boards can help you figure out how to enter your BIOS or
UEFI to locate and activate those settings. If those settings are not nested
under the Advanced tab, you might find them under the Security tab.

## Pre-installation


### Making a USB stick for installation

Recommendation: use a device with a read only switch and secure firmware, e.g. [Kangaru FlashTrust 8GB ~$30](https://www.kanguru.com/storage-accessories/kanguru-flashtrust-secure-firmware.shtml)

[Download](https://www.qubes-os.org/downloads/) the latest Qubes ISO.

[Verify its authenticity](https://www.qubes-os.org/security/verifying-signatures) before continuing.


#### Windows ISO to USB

Use the [Rufus](https://rufus.akeo.ie/) tool to write the
ISO to a USB key. Be sure to select "Write in DD Image mode" *after* selecting
the Qubes ISO and pressing "START" on the Rufus main window.

[![Rufus menu](https://www.qubes-os.org/attachment/doc/rufus-menu.png)](/attachment/doc/rufus-menu.png)

[![Rufus DD image mode](https://www.qubes-os.org/attachment/doc/rufus-dd-image-mode.png)](/attachment/doc/rufus-dd-image-mode.png)

## Installation

### Getting to the install screen

To install Qubes OS, you'll need to access your computer's BIOS or
UEFI menu so that you can tell it to boot from the USB drive to which you just
copied the Qubes installer ISO.

To begin, power off your computer and plug the USB drive into a USB port, but
don't press the power button yet. Right after you press the power button,
you'll have to immediately press a specific key to enter the BIOS or UEFI menu.
The key to press varies from brand to brand.

`Esc`, `Del`, and `F10` are common ones. ThinkPads use `Enter`

If you're not sure, you can search the web for `<COMPUTER_MODEL> BIOS
key` or `<COMPUTER_MODEL> UEFI key` (replacing `<COMPUTER_MODEL>` with your
specific computer model) or look it up in your computer's manual.

Once you know the key to press, press your computer's power button, then
repeatedly press that key until you've entered your computer's BIOS or UEFI
menu. 

Here's an example of what the BIOS menu looks like on a ThinkPad T430:

[![ThinkPad T430 BIOS menu](https://www.qubes-os.org/attachment/doc/Thinkpad-t430-bios-main.jpg)](/attachment/doc/Thinkpad-t430-bios-main.jpg)

And here's an example of what a UEFI menu looks like:

[![UEFI menu](https://www.qubes-os.org/attachment/doc/uefi.jpeg)](/attachment/doc/uefi.jpeg)

Once you access your computer's BIOS or UEFI menu, you'll want to go to the
"boot menu," which is where you tell your computer which devices to boot from.

The goal is to tell the computer to boot from your USB drive so that you can
run the Qubes installer. If your boot menu lets you select which device to boot
from first, simply select your USB drive. 

If, on the other hand, your
boot menu presents you with a list of boot devices in order, then you'll want
to move your USB drive to the top so that the Qubes installer runs before
anything else.

Once you're done on the boot menu, save your changes. How you do this depends
on your BIOS or UEFI, but the instructions should be displayed right there on
the screen or in a nearby tab. 

 Once your BIOS or
UEFI is configured the way you want it, reboot your computer. This time, don't
press any special keys. Instead, let the BIOS or UEFI load and let your
computer boot from your USB drive. If you're successful in this step, after a
few seconds you'll be presented with the Qubes installer screen:

[![Boot screen](https://www.qubes-os.org/attachment/doc/boot-screen.png)](/attachment/doc/boot-screen.png)

**When installing Qubes OS 4.0 on UEFI, there is intentionally no boot menu. It goes straight to the installer. 
The boot menu will be back in Qubes OS 4.1.**

From here, you can navigate the boot screen using the arrow keys on your
keyboard. Pressing the "Tab" key will reveal options. You can choose one of
three options:

* Install Qubes OS
* Test this media and install Qubes OS
* Troubleshooting
 
Select the option to install Qubes OS. 

If the boot screen does not appear, there are several options to troubleshoot.
First, try rebooting your computer. If it still loads your currently installed
operating system or does not detect your installation medium, make sure the
boot order is set up appropriately. The process to change the boot order varies
depending on the currently installed system and the motherboard manufacturer.
If **Windows 10** is installed on your machine, you may need to follow specific
instructions to change the boot order. This may require an [advanced
reboot](https://support.microsoft.com/en-us/help/4026206/windows-10-find-safe-mode-and-other-startup-settings).

### The installer home screen

On the first screen, you are asked to select the language that will be used
during the installation process. When you are done, select **Continue**.

[![welcome](https://www.qubes-os.org/attachment/doc/welcome-to-qubes-os-installation-screen.png)](/attachment/doc/welcome-to-qubes-os-installation-screen.png)

Prior to the next screen, a compatibility test runs. If the test fails, a window will pop up. 

[![Unsupported hardware detected](https://www.qubes-os.org/attachment/doc/unsupported-hardware-detected.png)](/attachment/doc/unsupported-hardware-detected.png)

This may simply indicate that IOMMU-virtualization hasn't been
activated in the BIOS or UEFI.

**Do not click the continue button if this message appears**

Return to the [hardware requirements](#hardware-requirements) section to activate virtualization.

If the test passes, you will reach the installation summary screen. 

### Installation summary

The Installation summary screen allows you to change how the system will be
installed and configured, including localization settings. At minimum, you are
required to select the storage device on which Qubes OS will be installed. 

[![Installation summary not ready](https://www.qubes-os.org/attachment/doc/installation-summary-not-ready.png)](/attachment/doc/installation-summary-not-ready.png)

### Software

[![Add-ons](https://www.qubes-os.org/attachment/doc/add-ons.png)](/attachment/doc/add-ons.png)

On the software selection tab, you can choose which software to install in
Qubes OS. 

* **Debian:** Unless you know what this is, you do not need to select it.
* **Whonix:** Whonix lets you route some or all of your network traffic through Tor for
greater privacy. You should install this.

Press **Done** to go back to the installation summary screen.

### Installation destination

Under the System section, you must choose the installation destination. Select
the storage device on which you would like to install Qubes OS. This should be your main hard drive.

[![Select storage device](https://www.qubes-os.org/attachment/doc/select-storage-device.png)](/attachment/doc/select-storage-device.png)

Qubes will fully encrypt your disk by default.

As soon as you press **Done**, the installer will ask you to enter a passphrase
for disk encryption. The passphrase should be complex. Make sure that your
keyboard layout reflects what keyboard you are actually using. When you're
finished, press **Done**.

**If you forget your passphrase there is no way to recover access to your data.**

[![Select storage passhprase](https://www.qubes-os.org/attachment/doc/select-storage-passphrase.png)](/attachment/doc/select-storage-passphrase.png)

When you're ready, press **Begin Installation**.

[![Installation summary ready](https://www.qubes-os.org/attachment/doc/installation-summary-ready.png)](/attachment/doc/installation-summary-ready.png)

### Create your user account

While the installation process is running, you can create your user account.
This is what you'll use to log in after disk decryption and when unlocking the
screen locker. By design, Qubes OS is a single-user operating system, so this user account is just for you.

Select **User Creation** to define a new user with administrator privileges and
a password.

The root account is deactivated and should remain as such, so you do not need to do anything with the root option.

[![Account name and password](https://www.qubes-os.org/attachment/doc/account-name-and-password.png)](/attachment/doc/account-name-and-password.png)

When the installation is complete, press **Reboot**. Don't forget to remove the
installation medium (external USB stick), or else you may end up seeing the installer boot screen
again.

## Post-installation

### First boot

If the installation was successful, you will be asked to enter your encryption passphrase.

### Initial Setup

You're almost done. Before you can start using Qubes OS, some configuration is
needed. 

[![Initial setup menu](https://www.qubes-os.org/attachment/doc/initial-setup-menu.png)](/attachment/doc/initial-setup-menu.png)

By default, the installer will create a number of qubes (depending on the
options you selected during the installation process). These are designed to
give you a more ready-to-use environment from the get-go.

[![Initial setup menu configuration](https://www.qubes-os.org/attachment/doc/initial-setup-menu-configuration.png)](/attachment/doc/initial-setup-menu-configuration.png)

Let's briefly go over the options:

* **Create default system qubes:**
  These are the core components of the system, required for things like
  internet access.
* **Create default application qubes:**
  These are how you compartmentalize your digital life. There's nothing special
  about the ones the installer creates. They're just suggestions that apply to
  most people. If you decide you don't want them, you can always delete them
  later, and you can always create your own.
* **Create Whonix Gateway and Workstation qubes:**
  You should select this option.
  * **Enabling system and template updates over the Tor anonymity network using
  Whonix:**
  If you select this option, then whenever you install or update software in
  dom0 or a template, the internet traffic will go through Tor.
* **Create USB qube holding all USB controllers:**
  Just like the network qube for the network stack, the USB qube isolates the
  USB controllers. You should select this option.
  * **Use sys-net qube for both networking and USB devices:**
  You should not select this option unless you rely on a USB device for network access,
  such as a USB modem or a USB Wi-Fi adapter. (should not be needed with our recommended laptops)
* **Do not configure anything:**
  This is for very advanced users only. If you select this option, you'll have
  to set everything up manually afterward. Do not select this.

When you're satisfied with you choices, press **Done**. This configuration
process may take a while, depending on the speed and compatibility of your
system.

After the configuration is done, you will be greeted by the login screen. Enter
your password and log in.

[![Login screen](https://www.qubes-os.org/attachment/doc/login-screen.png)](/attachment/doc/login-screen.png)

Congratulations, you are now ready to use Qubes OS!

[![Desktop menu](https://www.qubes-os.org/attachment/doc/desktop-menu.png)](/attachment/doc/desktop-menu.png)

## Next steps

### Updating

Next, [update](https://www.qubes-os.org/doc/how-to-update/) your installation to ensure you have
the latest security updates. Frequently updating is one of the best ways to
remain secure against new threats.

### Security

The Qubes OS Project occasionally issues [Qubes Security Bulletins
(QSBs)](https://www.qubes-os.org/security/qsb/) as part of the [Qubes Security Pack
(qubes-secpack)](https://www.qubes-os.org/security/pack/). It is important to make sure that you
receive all QSBs in a timely manner so that you can take action to keep your
system secure. (While [updating](#updating) will handle most security needs,
there may be cases in which additional action from you is required.) For this
reason, we strongly recommend that every Qubes user subscribe to the
[qubes-announce](https://www.qubes-os.org/support/#qubes-announce) mailing list.

### Backups

It is extremely important to make regular backups so that you don't lose your
data unexpectedly. The [Qubes backup
system](https://www.qubes-os.org/doc/how-to-back-up-restore-and-migrate/) allows you to do this
securely and easily.

### Please submit your Hardware Compatability report

This will help other jungle animals choose and buy compatible laptops and will help the QubesOS project. It takes two minutes. Please see
[generating and submitting a Hardware Compatibility List (HCL)
report](https://www.qubes-os.org/doc/how-to-use-the-hcl/#generating-and-submitting-new-reports).

## Getting help

* Ask BowTiedIguana on Twitter or Discord

* If issues arise during installation, see the [Installation
  Troubleshooting](https://www.qubes-os.org/doc/installation-troubleshooting) guide. 

* Check the [documentation](https://www.qubes-os.org/doc/): QubesOS documentation team work very hard to make the [documentation](https://www.qubes-os.org/doc/) accurate, comprehensive  useful and user friendly.

* If you don't find your answer in the documentation, please see [Help,
  Support, Mailing Lists, and Forum](https://www.qubes-os.org/support/) for places to ask.
