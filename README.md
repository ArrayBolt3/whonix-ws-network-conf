# Network Configuration for Whonix-Workstation #

Includes /etc/network/interfaces for Whonix-Workstation.

Sets up an internal network interface eth0.

DNS configuration Anonymity Linux Distribution Workstations
Whether a Anonymity Linux Distribution Gateway supports anonymized system DNS
for Workstation's traffic (also known as Transparent DNS Proxy) mainly depends
on the Gateway's firewall.

This package is simply installing /etc/resolv.conf which points to
10.152.152.10, where an Anon-Gateway is supposed to provide a DnsPort on port
53.

Currently relevant for Non-Qubes-Whonix only.
## How to install `whonix-ws-network-conf` using apt-get ##

1\. Download [Whonix's Signing Key]().

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `whonix-ws-network-conf`.

```
sudo apt-get install whonix-ws-network-conf
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions. (Replace `generic-package` with the actual name of this package `whonix-ws-network-conf`.)

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`whonix-ws-network-conf` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
