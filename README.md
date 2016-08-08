
 Google Material design icons adaptation for Magento 2
 Version: 0.01

 Created by Victor Slivinsky
 07.08.2016

 This lib extend default Google Material icons lib. Just copy web folder to your Magento 2 Theme folder and import "_material-design-icons.less" file for example to "_sources.less".

 I have implemented 2 extra variants of  usage Material design icons:

 1 - Individual usage. Allows set icons as ":before" element for any page element.
     You don't need to modify template files. Use this structure
```
.any_class_name:before {
      &:extend(.material-icons);
      content: 'label'; /* Use numeric character for ie10 and earlier "\E87C" */
}
```

 2 - BEM Model. Based on 2 classes:
 ".material-icons" -as element class and
 ".material-star"  -as class modificator
 create an inline element with the appropriate classes, like so:
```
 <a href="#"><span class="material-icons material-star"></span> Star</a>
 ```
 There "star" is name of icon. You can find all names and connected on Google page:
 https://design.google.com/icons/

 Use @icon-font-path: for load fonts. This variable includes path default for Magento.
 It is relative path from YourTheme/web/css folder.