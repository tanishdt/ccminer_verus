# ccminer_verus
Mine Verus Coin (VRSC) on Android using ccminer! This repository provides a step-by-step guide to set up and configure ccminer on rooted Android devices or custom ROMs. Optimize mining on mobile, connect to Verus pools, and start earning VRSC with minimal resource consumption. Perfect for mobile miners!

# Verus Coin Mining on Android with ccminer

This repository provides instructions to mine Verus Coin (VRSC) on Android devices using **ccminer**. Follow the steps below to set up your mobile mining rig.

## Prerequisites

- **Linux Knowledge**: Some fundamental Linux knowledge is required. Brush up on it via an online course if needed.
- **Linux Screen**: Learn how to use `screen` for long-term mining sessions.
- **SSH and SCP**: Recommended for remote management.
- **Stable Network**: Ensure a stable WiFi or cellular connection.

## Installation Instructions

1. **Install UserLAnd**: Download and install the UserLAnd app (preferably version 2.8.3 from the app store or APK).
2. **Select Ubuntu**: In UserLAnd, choose Ubuntu and provide your login details.
3. **Choose SSH**: Select the SSH option and wait for Ubuntu to install.
4. **Log In**: Once installed, log in to your Ubuntu account.
5. **Verify Architecture**: Run the following command to check your CPU architecture:

```
lscpu
```

- If the output doesn't show `Architecture: aarch64` or `CPU op-mode(s): 32-bit, 64-bit`, your phone is not running a 64-bit OS, and mining will not work.

6. **Install Mining Script**:
```
curl -o- -k https://raw.githubusercontent.com/tanishdt/ccminer_verus/main/install.sh | bash
```

8. **Configure Mining Settings**:
- Open `config.json`:
  ```
  nano config.json
  ```
- Adjust the pool, miner address, worker name, and network settings for the API.
- Save and exit by pressing `<CTRL>-X`, then `Y` and `<ENTER>`.

8. **Start Mining**:
- Start the miner with:
  ```
  ~/ccminer/start.sh
  ```
***Inspiration taken from https://github.com/TheRetroMike/VerusCliMining***
