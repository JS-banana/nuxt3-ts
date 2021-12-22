# nuxt-vue3-ts

期待目标结果为 nuxt3，即 vite + vue3 + ts的技术栈支持

目前nuxt3还处于 [beta](https://v3.nuxtjs.org/)版本，该项目当前方案为：使用 [nuxt2](https://nuxtjs.org/)的脚手架进行完整搭建的vue2项目，不过本人目前比较嫌弃vue2，因此采取了间接方案，nuxt官方提供的 [Bridge](https://v3.nuxtjs.org/getting-started/bridge#bridge)，因此，这里只是过渡版本，主要作用为熟悉 nuxt的开发环境

这里 Bridge的主要作用相当于提前使用了nuxt3的一些相关技术方案，vite、vue3等

三条线：

- 直接使用 nuxt2进行上手实战开发
- 使用 nuxt3抢先上手体验
- nuxt2 + bridge的过渡版本

## Build Setup

静态模式 `target: 'static'`不使用 `yarn start`

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```
