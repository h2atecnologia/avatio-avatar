#Avatio Avatar

VueJS 2 component to display SVG avatar.

<p align="center"><img src='https://img.avatio.cool/avatar.svg?sex=Female&options%5BFemaleHeadShape%5D%5Bcolor%5D=%23DBA582&options%5BEyes%5D%5Btype%5D=C&options%5BEyes%5D%5Bcolor%5D=%23634e34&options%5BMouth%5D%5Btype%5D=B&options%5BMouth%5D%5Bcolor%5D=%23C13539&options%5BFemaleHair%5D%5Btype%5D=G&options%5BFemaleHair%5D%5Bcolor%5D=%23554838&options%5BFemaleGlasses%5D%5Btype%5D=B&options%5BFemaleGlasses%5D%5Bcolor%5D=%237f8c8d&options%5BFemaleClothes%5D%5Btype%5D=F&options%5BFemaleClothes%5D%5Bcolor%5D=%2316a085&options%5BFemaleClothes%5D%5BsecondaryColor%5D=%23f1c40f&options%5BFemaleAccessory%5D%5Btype%5D=FemaleB&options%5BFemaleAccessory%5D%5Bcolor%5D=%23f1c40f&options%5BNose%5D%5Bcolor%5D=%23ef843b' style='width: 300px; height: 300px;' /></p>

Vector graphic is designed by [Teneresa](https://github.com/teneresa) - and therefore I ow her a big thank you!

Inspiration came from [Avataaars](https://github.com/fangpenlin/avataaars/), which is similar project focusing on React.

## Features

* SVG
* Configurable
* Extensible

## How to use

At first you have to install package by yarn or npm like so

```bash
yarn add avatio-avatar
```

Then you can use the component

```javascript
import Avatar, {Config} from 'avatio-avatar';

const app = new Vue({
    components: {Avatar},
    template: `<avatar :config="config" :options="options"></avatar>`,
    data: {
        config: Config['Female'],
        options: {
          FemaleGlasses: {
            color: "#fff",
            type: "B",
          },
          //...
        },
    }
});

```

## Configuration

All component is dynamical and is generated by configuration, [take a look](https://github.com/trunda/avatio-avatar/blob/master/src/avatio.js).
By this mechanism is easily extensible and config is used to generate [UI of avatar generator](https://github.com/trunda/avatio-ui).

## Building 

If you want to build the package, you can run

```bash
yarn build
```
