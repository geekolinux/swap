## Swap role for all common Linux distributions
Features of my swap repository:
- [x] Create a swap file with a custom size 
- [x] Create a swap file with a precalculated arithmetic operation from the official redhat documentation [Swap Calculation](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-swapspace).
- [x] Disable/Enable the swap space in your system
- [x] Customization of the swap file
- [x] Debian, Ubuntu, RedHat, CentOS, AlmaLinux, Oracle, Suse


## Requirements
To run the playbook on your target hosts, you need to install following packages:
- util-linux

Debian, Ubuntu:

``sudo apt-get install util-linux``

RedHat, CentOS, Oracle, AlmaLinux:

``sudo dnf install util-linux``

Suse, openSuse:

``sudo zypper install util-linux``


  
## Usage
If you want to create the swap file with the calculation formular from RedHat and enable it immediately, use these variables:
```yaml
swap_create: "true"
swap_enable: "true"
```
Customize the swap file with a specific size:
```yaml
swap_custom_size_mb: "4096"
swap_custom: "true"
```

Change the metadata of the swap file
```yaml
swap_file: "/swapfile"
swap_file_owner: "root"
swap_file_group: "root"
swap_file_perm: "0600"
```
Disable the swap file:
```yaml
swap_enable: "false"
```


## License
[MIT License](https://opensource.org/license/MIT)

## Author
I like to give linux administrators an guidance and solving their hand-made problems with the new generation of automatization.
I´m open for any improvements, please contact if you have an feature requests to make my repository better. Feedback is always welcome, just write me 
on my email: geekolinuxexpert@proton.me

Enjoy my art,

Geeko
