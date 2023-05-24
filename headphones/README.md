# Headphones

The Headphones script is a bash script that allows you to connect or pair Bluetooth headphones with your device. It reads the MAC address of the headphones from an environment variable.

## Prerequisites

- `bluetoothctl`: Make sure `bluetoothctl` command-line tool is installed on your system.

## Setup

1. Clone the repository or download the script file.
2. Create a file named `.env` in the same directory as the script.
3. Open the `.env` file in a text editor and set the value of the `HEADPHONES_MAC` variable to the MAC address of your headphones. Example: `HEADPHONES_MAC=00:11:22:33:44:55`.
4. Save the `.env` file.
5. Make the script file (`headphones`) executable by running `chmod +x headphones`.

## Usage

To use the Headphones script, open a terminal and navigate to the directory where the script is located. Then, run the following command:

```bash
./headphones [OPTION]
```

Replace `[OPTION]` with one of the following:

- `-p` or `--pair`: Pair the device with the headphones instead of connecting.
- `-h` or `--help`: Show help information.

If no option is provided, the script will attempt to connect to the headphones using the MAC address stored in the `HEADPHONES_MAC` environment variable.

## Alias

To simplify the usage of the Headphones script, you can create an alias in your shell configuration file (`~/.bashrc`, `~/.bash_profile`, etc.). For example, you can add the following line:

```bash
alias hp='/path/to/headphones'
```

After adding the alias, you can use the `hp` command instead of `./headphones` to execute the script.

## Example

Connect to headphones:
```bash
./headphones
```
or
```bash
hp
```

Pair headphones:
```bash
./headphones -p
```
or
```bash
hp -p
```

Display help information:
```bash
./headphones -h
```
or
```bash
hp -h
```
