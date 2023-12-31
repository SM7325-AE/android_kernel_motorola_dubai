# SPDX-License-Identifier: GPL-2.0-or-later
#
# Makefile for the linux exFAT filesystem support.
#

config EXFAT_FS
	tristate "exFAT filesystem support"
	select NLS
	help
	  This allows you to mount devices formatted with the exFAT file system.
	  exFAT is typically used on SD-Cards or USB sticks.

	  To compile this as a module, choose M here: the module will be called
	  exfat.

config EXFAT_DISCARD
	bool "enable discard support"
	depends on EXFAT_FS
	default y

config EXFAT_DELAYED_SYNC
	bool "enable delayed sync"
	depends on EXFAT_FS
	default n

config EXFAT_KERNEL_DEBUG
	bool "enable kernel debug features via ioctl"
	depends on EXFAT_FS
	default n

config EXFAT_DEBUG_MSG
	bool "print debug messages"
	depends on EXFAT_FS
	default n

config EXFAT_DEFAULT_CODEPAGE
	int "Default codepage for exFAT"
	default 437
	depends on EXFAT_FS
	help
	  This option should be set to the codepage of your exFAT filesystems.

config EXFAT_DEFAULT_IOCHARSET
	string "Default iocharset for exFAT"
	default "utf8"
	depends on EXFAT_FS
	help
	  Set this to the default input/output character set to use for
	  converting between the encoding that is used for user visible
	  filenames and the UTF-16 character encoding that the exFAT
	  filesystem uses.  This can be overridden with the "iocharset" mount
	  option for the exFAT filesystems.
