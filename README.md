
# Resume

Install MiKTeX for generating pdf from latex file.

https://miktex.org/download

## Linux Mint

```sh

curl -fsSL https://miktex.org/download/key | sudo tee /usr/share/keyrings/miktex-keyring.asc > /dev/null
echo "deb [signed-by=/usr/share/keyrings/miktex-keyring.asc] https://miktex.org/download/ubuntu jammy universe" | sudo tee /etc/apt/sources.list.d/miktex.list
sudo apt-get update
sudo apt-get install miktex
miktexsetup finish
sudo miktexsetup --shared=yes finish # for installing to all users
initexmf --set-config-value [MPM]AutoInstall=1 # set auto install of required library
sudo initexmf --admin --set-config-value [MPM]AutoInstall=1 # set auto install of required library for all users
sudo initexmf --admin --set-config-value "[MPM]AutoInstall=1" # set auto install of required library for all users if the above does not work

```