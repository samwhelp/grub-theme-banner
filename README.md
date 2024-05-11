

# Home

| Link | GitHub |
| ---- | ------ |
| [grub-theme-banner](https://samwhelp.github.io/grub-theme-banner/) | [GitHub](https://github.com/samwhelp/grub-theme-banner) |




## Subject

* [Background Source](#background-source)
* [Theme File](#theme-file)
* [Install](#install)
* [Apply](#apply)
* [Helper](#helper)
* [Docs](#docs)




## Background Source

* [iron man](https://www.reddit.com/r/wallpaper/comments/olengo/3840x2160_iron_man/)
* [https://i.redd.it/1ai3l6g54kb71.jpg](https://i.redd.it/1ai3l6g54kb71.jpg)




## Theme File

| Theme File                       |
| -------------------------------- |
| [theme.txt](https://github.com/samwhelp/grub-theme-banner/blob/main/theme.txt)           |
| [background.jpg](https://github.com/samwhelp/grub-theme-banner/blob/main/background.jpg) |




## Install

run

``` sh

mkdir -p "./tmp"

wget -c "https://github.com/samwhelp/grub-theme-banner/archive/refs/heads/main.tar.gz" -O "./tmp/grub-theme-banner-main.tar.gz"


tar xf "./tmp/grub-theme-banner-main.tar.gz" -C "./tmp"


sudo mkdir -p "/boot/grub/themes"

sudo cp -rf "./tmp/grub-theme-banner-main/." "/boot/grub/themes/grub-theme-banner"

```

or run remote script [fetch.sh](https://github.com/samwhelp/grub-theme-banner/blob/main/helper/theme-installer/fetch.sh)

``` sh
bash <(curl -L 'https://raw.githubusercontent.com/samwhelp/grub-theme-banner/main/helper/theme-installer/fetch.sh')
```




## Apply

edit `/etc/default/grub`

```
GRUB_BACKGROUND='/boot/grub/themes/grub-theme-banner/background.jpg'
GRUB_THEME="/boot/grub/themes/grub-theme-banner/theme.txt"
```

or create file `/etc/default/grub.d/theme.cfg`, run

``` sh
cat << EOF | sudo tee /etc/default/grub.d/theme.cfg
GRUB_BACKGROUND='/boot/grub/themes/grub-theme-banner/background.jpg'
GRUB_THEME="/boot/grub/themes/grub-theme-banner/theme.txt"

EOF
```


then run

``` sh
sudo update-grub
```

or run

``` sh
sudo grub-mkconfig -o /boot/grub/grub.cfg
```




## Helper

| Helper |
| ------ |
| [background-selector](https://github.com/samwhelp/grub-theme-banner/tree/main/helper/background-selector) |
| [style-selector](https://github.com/samwhelp/grub-theme-banner/tree/main/helper/style-selector) |
| [region-selector](https://github.com/samwhelp/grub-theme-banner/tree/main/helper/region-selector) |




## Docs

| Grub Docs |
| ---- |
| [Theme file format](https://www.gnu.org/software/grub/manual/grub/html_node/Theme-file-format.html) |




## Styled Boxes

| Region              | Region          | Region              |
| ------------------- | --------------- | ------------------- |
| 1. Northwest (`nw`) | 2. North (`n`)  | 3. Northeast (`ne`) |
| 4. West (`w`)       | 5. Center (`c`) | 6. East (`e`)       |
| 7. Southwest (`sw`) | 8. South (`s`)  | 9. Southeast (`se`) |

> menu-box file name

| Region               | Region              | Region               |
| -------------------- | ------------------- | -------------------- |
| 1. `menu-box-nw.png` | 2. `menu-box-n.png` | 3. `menu-box-ne.png` |
| 4. `menu-box-w.png`  | 5. `menu-box-c.png` | 6. `menu-box-e.png`  |
| 7. `menu-box-sw.png` | 8. `menu-box-s.png` | 9. `menu-box-se.png` |




## Branch

| Branch |
| --- |
| [main](https://github.com/samwhelp/grub-theme-banner/tree/main) |
| [gh-pages](https://github.com/samwhelp/grub-theme-banner/tree/gh-pages) |
