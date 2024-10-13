
# Debian 12 (Bookworm) Sources List for Intel x86

![Debian](debian.png)

This repository contains a pre-configured `sources.list` file for Debian 12 (Bookworm) on Intel x86 architecture. This file can be used to replace or modify the default `sources.list` on a Debian system to ensure access to all relevant repositories, including the main, contrib, non-free, non-free-firmware, security updates, and backports.

## Purpose

When setting up a Debian system, the `/etc/apt/sources.list` file is used by the package manager `apt` to determine where to find and download software packages. This repository provides a reliable and optimized `sources.list` for Debian 12 users on Intel x86 architecture. It includes the official Debian repositories as well as backports, security updates, and support for non-free and non-free-firmware packages.

## Repository Structure

```
.
├── README.md        # Documentation on how to use the repository
└── sources.list     # Pre-configured sources.list file for Debian 12 x86
```

## How to Use

### Step 1: Backup Your Current sources.list

Before modifying your `/etc/apt/sources.list`, it's always a good idea to make a backup of the existing file. Run the following command in your terminal:

```bash
sudo cp /etc/apt/sources.list /etc/apt/sources.list.backup
```

This will create a backup of the original file in case you need to restore it later.

### Step 2: Clone the Repository

Clone this repository to your local machine using `git`:

```bash
git clone https://github.com/yourusername/debian12.git
```

Navigate to the directory:

```bash
cd debian12
```

### Step 3: Replace Your sources.list

Copy the pre-configured `sources.list` file from the repository to your system's `/etc/apt/` directory:

```bash
sudo cp sources.list /etc/apt/sources.list
```

### Step 4: Update Package Sources

After replacing the `sources.list` file, update your package lists to reflect the changes:

```bash
sudo apt update
```

This will download the latest information about available packages and ensure that you're connected to the correct repositories.

## What's Included

The `sources.list` file provided includes the following repositories:

- **Main**: The core repository containing free and open-source software officially supported by Debian.
- **Contrib**: Includes free software that depends on non-free components.
- **Non-free**: Contains software that is not free, such as drivers and firmware.
- **Non-free-firmware**: Includes firmware that may be required for some hardware, especially network adapters.
- **Security Updates**: Ensures that your system receives important security patches.
- **Backports**: Provides access to newer versions of software that are not yet in the main repository.

## Example of sources.list

Below is the content of the `sources.list` file included in this repository:

```bash
# Debian 12 (Bookworm) main repositories
deb http://deb.debian.org/debian/ bookworm main contrib non-free non-free-firmware
deb-src http://deb.debian.org/debian/ bookworm main contrib non-free non-free-firmware

# Debian 12 (Bookworm) updates
deb http://deb.debian.org/debian/ bookworm-updates main contrib non-free non-free-firmware
deb-src http://deb.debian.org/debian/ bookworm-updates main contrib non-free non-free-firmware

# Security updates
deb http://deb.debian.org/debian-security bookworm-security main contrib non-free non-free-firmware
deb-src http://deb.debian.org/debian-security bookworm-security main contrib non-free non-free-firmware

# Backports (optional, if you want newer versions of some packages)
deb http://deb.debian.org/debian/ bookworm-backports main contrib non-free non-free-firmware
deb-src http://deb.debian.org/debian/ bookworm-backports main contrib non-free non-free-firmware
```

## Contributions

We welcome contributions to improve this repository. If you have suggestions for improvements or additional configurations that should be included, feel free to open a pull request or create an issue. Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-feature`.
3. Make your changes and commit them: `git commit -am 'Add your feature'`.
4. Push to the branch: `git push origin feature/your-feature`.
5. Open a pull request to discuss and review the changes.

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## Support

If you encounter any issues or have any questions, feel free to open an issue in the repository or contact the maintainer.

---

Thank you for using this repository! Feel free to share it with others who may find it helpful.
# Debian12
