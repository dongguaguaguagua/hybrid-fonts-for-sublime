# Hybrid fonts for sublime text 4

In VScode, users can use two fonts by installing a custom css plugin and changing css styles.

But there is no way changing css in sublime text 4. But sublime can detect bold and italic fonts in a font family. For example, Fira Code is a font family, which contains Bold,Light,Medium,SemiBold,Regular,Retina fonts.

`"font_face": "Fira Code",` in Preferences.sublime-settings tells sublime to use the fira code font family. My sublime can only distinguish FiraCode-Italic and FiraCode-Bold.

When FiraCode-Italic doesn't exisit, sublime will fake the italic font. However, it fails to fake the bold font if FiraCode-Bold is not found. In this case, a text dosn't change when it sopposed to be bold.

## Fira-Code-60002

This folder contains 8 ttf fonts:

```
FiraCode-Bold.ttf     FiraCode-Medium.ttf   FiraCodeRegular-OperatorMonoLightItalic.ttf
FiraCode-SemiBold.ttf FiraCode-Regular.ttf  FiraCodeRegular-ConsolasItalic.ttf
FiraCode-Light.ttf    FiraCode-Retina.ttf
```

### Fira Code & Consolas

Please rename `Fira-Code-60002/FiraCodeRegular-ConsolasItalic.ttf` into `FiraCode-Italic.ttf` then install it.

Up till 2023/1/9, the latest Fira Code version is 6.2, but obviously, FiraCode 6.2 doesn't provide an italic font. So I combined Fira Code with [consolas_ligaturized](https://github.com/somq/consolas-ligaturized).

To be more specefic, I extracted italic characters *ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789* and punctuation marks like *'"/!@#$%^&* from consolas and migrated them with Fira Code Regular.

As a result, the hybrid font *Fira Code Italic* is similiar with consolas but maintained ligature feature of Fira Code.

![ligature Image](https://raw.githubusercontent.com/dongguaguaguagua/hybrid-fonts-for-sublime/main/images/Snipaste_2023-01-09_19-47-53.png)

Other fonts in Fira-Code-60002 are exactly the same fonts from the latest Fira Code github release.

Also, *Fira Code Italic* belongs to Fira Code font family, so you can install this font to your computer with no concern.

It looks pretty in both Python and C++, with Monakai Pro (code scheme) and Material Theme (UI).

![Python Image](https://raw.githubusercontent.com/dongguaguaguagua/hybrid-fonts-for-sublime/main/images/Snipaste_2023-01-09_19-20-28.png)

![Cpp Image](https://raw.githubusercontent.com/dongguaguaguagua/hybrid-fonts-for-sublime/main/images/Snipaste_2023-01-09_19-24-30.png)

### Fira Code & operator mono light italic

Please rename `Fira-Code-60002/FiraCodeRegular-OperatorMonoLightItalic.ttf` into `FiraCode-Italic.ttf` then install it.

Looks good on my mac:

![Cpp Image](https://raw.githubusercontent.com/dongguaguaguagua/hybrid-fonts-for-sublime/main/images/Snipaste_2023-01-09_20-33-56.png)

### Fira Code Regular With Changed `g` and `a`

In [Fira Code WiKi](https://github.com/tonsky/FiraCode/wiki/How-to-enable-stylistic-sets), code cv01 and code cv02 mean to change the style of `g` and `a`. But sublime doesn't provide cv01 and cv02. So I have to edit the ttf file myself.

![stylistic settings](https://raw.githubusercontent.com/dongguaguaguagua/hybrid-fonts-for-sublime/main/images/Snipaste_2023-01-10_12-21-51.png)

## Monaco



## How to build your own hybrid font ?



