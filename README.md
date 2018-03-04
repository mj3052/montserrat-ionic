# montserrat-ionic
 
## Instalação da font
```
$ npm i montserrat-ionic --save
```
## Editar os arquivos

node_modules/@ionic/app-scripts/config/sass.config.js

de:
  ```
  /**
   * includePaths: Used by node-sass for additional
   * paths to search for sass imports by just name.
   */
  includePaths: [
    'node_modules/ionic-angular/themes',
    'node_modules/ionicons/dist/scss',
    'node_modules/ionic-angular/fonts'
  ],
```
  para:
  ```
  /**
   * includePaths: Used by node-sass for additional
   * paths to search for sass imports by just name.
   */
  includePaths: [
    'node_modules/ionic-angular/themes',
    'node_modules/ionicons/dist/scss',
    'node_modules/ionic-angular/fonts',
    'node_modules/montserrat-ionic/scss'
  ],
  ``` 

  node_modules/@ionic/app-scripts/config/copy.config.js

  de:
  ```
  copyFonts: {
    src: ['{{ROOT}}/node_modules/ionicons/dist/fonts/**/*', '{{ROOT}}/node_modules/ionic-angular/fonts/**/*'],
    dest: '{{WWW}}/assets/fonts'
  },
  ```
  para:
  ```
  copyFonts: {
    src: ['{{ROOT}}/node_modules/montserrat-ionic/fonts/**/*', '{{ROOT}}/node_modules/montserrat-ionic/scss/**/*', '{{ROOT}}/node_modules/ionicons/dist/fonts/**/*', '{{ROOT}}/node_modules/ionic-angular/fonts/**/*'],
    dest: '{{WWW}}/assets/fonts'
  },
  ```

 src/theme/variables.scss
  
 de:
```
// Fonts
// --------------------------------------------------

 @import "roboto";
 @import "noto-sans";

```
para:

```
// Fonts
// --------------------------------------------------

// @import "roboto";
// @import "noto-sans";
@import "montserrat";

$font-family-md-base: 'Montserrat-Light';
$font-family-ios-base: 'Montserrat-Light';

```