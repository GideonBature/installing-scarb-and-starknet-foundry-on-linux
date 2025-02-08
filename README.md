# **Installing Scarb and Starknet Foundry on Linux**

This guide will walk you through installing **Scarb** (the Cairo package manager) and **Starknet Foundry** on Linux using `asdf`.

## **1. Install Git**
Ensure Git is installed before proceeding:

- **Debian-based (e.g., Ubuntu):**  
  ```sh
  sudo apt install git -y
  ```
- **RHEL-based (e.g., Fedora):**  
  ```sh
  sudo dnf install git -y
  ```

## **2. Install `asdf` (Version Manager)**
`asdf` is not available in package managers by default, so install it manually:

```sh
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.13.1
echo '. "$HOME/.asdf/asdf.sh"' >> ~/.bashrc
echo '. "$HOME/.asdf/completions/asdf.bash"' >> ~/.bashrc
source ~/.bashrc
```

For **Zsh users** (instead of Bash):

```sh
echo '. "$HOME/.asdf/asdf.sh"' >> ~/.zshrc
echo '. "$HOME/.asdf/completions/asdf.zsh"' >> ~/.zshrc
source ~/.zshrc
```

## **3. Install `Scarb` (Cairo Package Manager)**
Add the `scarb` plugin and install the latest version:

```sh
asdf plugin add scarb
asdf install scarb latest
asdf global scarb latest
```

## **4. Verify `Scarb` Installation**
Run the following command:

```sh
scarb --version
```

If installed correctly, it should display the version.

## **5. Install `Starknet Foundry`**
Add the `starknet-foundry` plugin and install the latest version:

```sh
asdf plugin add starknet-foundry
asdf install starknet-foundry latest
asdf global starknet-foundry latest
```

## **6. Verify `Starknet Foundry` Installation**
Check if it was installed successfully:

```sh
snforge --version
sncast --version
```

---

### **You're all set! 🚀**
Now you can use **Scarb** for Cairo development and **Starknet Foundry** for testing and smart contract deployment. Let me know if you have any issues installing any of the packages/tools!
