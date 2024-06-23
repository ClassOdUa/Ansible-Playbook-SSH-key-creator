# Ansible Playbook to Create SSH Key Pair

This repository contains an Ansible playbook designed to automate the creation of SSH key pairs. The playbook prompts the user for necessary information, checks if an SSH key already exists for the specified host, and generates a new SSH key pair if it does not exist.

## Features

- Prompts the user for the SSH key storage folder, host name, host IP, and password for the SSH private key.
- Checks if an SSH key already exists for the given host.
- Generates a new SSH key pair using the specified cipher type (default: `ed25519`).
- Displays the fingerprint of the generated SSH key.

## Requirements

- Ansible 2.9 or higher
- `community.crypto` Ansible collection

## Installation

1. Install Ansible:
   ```sh
   sudo apt-get install ansible
   ```
Install the community.crypto collection:
   ```sh
   ansible-galaxy collection install community.crypto
   ```
## Usage

1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/ansible-ssh-keygen.git
   cd ansible-ssh-keygen
   ```
2. Run the playbook:
   ```sh
   ansible-playbook create_ssh_key.yml
   ```
3. Follow the prompts to provide the necessary information:
- Define the SSH key pair storage folder (default: ~/.ssh).
- Define the host name (default: example.local).
- Define the host IP (default: 0.0.0.0).
- Define the password for the SSH private key.

## Example
   ```sh
   ansible-playbook create_ssh_key.yml
  
   Define the SSH key pair storage folder: ~/.ssh
   Define the Host Name: myserver.local
   Define the Host IP: 192.168.1.100
   Define the password for SSH Private Key: ********
   ```
## License

This project is licensed under the MIT License.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes or enhancements.
