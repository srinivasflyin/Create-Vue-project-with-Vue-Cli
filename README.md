# Creating Vue Project with Vue Cli

## Project setup
```
npm install
```

### Compiles and minifies for production
```
npm run build
```
### Run your production build locally 
```
npx serve dist
```

### Run your unit tests
```
npm run test:unit
```

### Run your end-to-end tests
```
npm run test:e2e
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

Here i have used Vue cli with typescript support, when your creating Vue project with Vue Cli it shows the list of options to select: 


Typescript

list of testing libraries

Vuex support

Vue router support

Axios support


After completion of steps your project will be ready to run.
We will use the Vue property decorator to create the Vue components with extending of Vue.

        <template>
         <div>
           <div v-for="item in items" :key="item.name">
              <img :src="getImgUrl(item.imgUrl)" :alt="item.name"/>
              <span>{{item.name}}</span>
          </div>
        </div>
        </template>
        
        <script lang="ts">
        import { Vue, Component, Prop } from 'vue-property-decorator'
        import {} from '../shared/classesAndInterfaces'
        @Component
        export default class List extends Vue {
            @Prop() public items!: object []
            getImgUrl(imageUrl: string): string {
                return require(`../assets/hotelImages/${imageUrl}`)
            }
        }
        </script>
        
### Compiles and hot-reloads for development
```
npm run serve
```        
