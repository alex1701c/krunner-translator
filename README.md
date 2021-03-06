# Translator for KDE KRunner (Plasma 5)

This is a plugin for Plasma 5 KRunner. It's a translator and it translates text. Currently [glosbe](https://glosbe.com/) and [yandex](https://www.yandex.ru/) are supported.

## Installation ##
#### Required Dependencies
Debian/Ubuntu:  
`sudo apt install cmake extra-cmake-modules build-essential libkf5runner-dev libkf5textwidgets-dev qtdeclarative5-dev gettext`

openSUSE  
`sudo zypper install cmake extra-cmake-modules libQt5Widgets5 libQt5Core5 libqt5-qtlocation-devel ki18n-devel ktextwidgets-devel 
kservice-devel krunner-devel gettext-tools kconfigwidgets-devel`

Fedora  
`sudo dnf install cmake extra-cmake-modules kf5-ki18n-devel kf5-kservice-devel kf5-krunner-devel kf5-ktextwidgets-devel gettext`

```
mkdir build
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=`kf5-config --prefix` -DKDE_INSTALL_QTPLUGINDIR=`kf5-config --qt-plugins` -DCMAKE_BUILD_TYPE=Release
make 
sudo make install
kquitapp5 krunner
krunner
```
## Configuration ##

For being able to use yandex, an api key is required. You have to obtain a key yourself by following these steps:  
1. Register at https://passport.yandex.com/  
2. Get a API key at https://tech.yandex.com/keys/get/?service=trnsl   
3. Copy the key to the configuration dialog  

If you do not provide an api key only the translation via glosbe will work.

## Usage ##

A list of all language codes you can find [here](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).

### Specify source and target language ###
Syntax: \<sourcelang\>-\<targetlang\> \<searchterm\>  
*en-de house* → will translate *house* into german (*de*)

### Use default source language ###
Syntax: \<targetlang\> \<searchterm\>

Default source language: *English (en)*  
Alternative source language: *German (de)*  

*de soccer* → *en-de soccer*  
*en blau* → *de-en blau*  
*fr house* → *en-fr house*  

Thanks for your feedback and kudos! If you like the runner, please vote for it [here](http://kde-apps.org/content/show.php?content=156498).
  
