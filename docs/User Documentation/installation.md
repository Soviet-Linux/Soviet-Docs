# Installation Instructions

**[Soviet-Linux](https://github.com/Soviet-Linux) is not suitable for daily use. However, you can test it by following the instructions below.**  
You can try out [Soviet-Linux](https://github.com/Soviet-Linux) in three different ways.

## 1. Using Docker

### Prerequisites

1. Podman or Docker (Podman is recommended)

### Running the container

>Note: If you want this container to preserve changes you've made, remove `--rm`.

```bash
docker run -it --rm ghcr.io/soviet-linux/soviet:latest /bin/bash
```

## 2. Using chroot

1. Download the image
   To download a testing release you need to join our [Discord Server](https://discord.gg/P95xPM9KZY) after you join head to the [#testing-releases channel](https://discord.com/channels/959403569302343682/1053639049476321340) and download the latest image
2. Unpack the image
    After you donwload the image to unpack it just run:

    ```
    tar -xf "/path/to/soviet.tar.gz"
    ```

3. Create chroot
    To create the chroot environment you just run:

    ```
    sudo chroot "/path/to/soviet"
    ```

## 3. Using systemd-nspawn

### Prequisites

- Systemd (required for systemd-nspawn) if you dont have systemd you can use [chroot](#2-using-chroot)

### Creating systemd-nspawn

1. Download the image
   To download a testing release you need to join our [Discord Server](https://discord.gg/P95xPM9KZY) after you join head to the [#testing-releases channel](https://discord.com/channels/959403569302343682/1053639049476321340) and download the latest image
2. Unpack the image
    After you donwload the image to unpack it just run:

    ```
    tar -xf "/path/to/soviet.tar.gz"
    ```

3. Create systemd-nspawn
    To create the systemd-nspawn environment you just run:

    ```
    systemd-nspawn -bD "/path/to/soviet"
    ```

## Login Credentials

- Username: root
- Password: sovietlinux

