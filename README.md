# DFSnippets - VS Code Uzantısı

## Genel Bakış

DFSnippets, VS Code kullanıcıları için özel olarak oluşturulmuş bir snippet (parçaçık) koleksiyonudur. Bu snippet'ler, yazılım geliştirme sürecinizde sık kullandığınız kod kalıplarını hızlı bir şekilde eklemenizi sağlar.

## Özellikler

- DFS algoritmasına yönelik sık kullanılan kod parçalarını içerir.
- Özelleştirilmiş snippet isimleri ve tetikleyicileri sayesinde kolay kullanım sağlar.
- Hızlı ve verimli geliştirme için optimize edilmiştir.

## Nasıl Kullanılır

1. VS Code'u açın ve "Extensions" sekmesine gidin.
2. "DFSnippets" yazarak uzantıyı arayın ve yükleyin.
3. Bir dosyada çalışırken, uygun bir kod parçasını eklemek için ilgili snippet tetikleyicisini kullanın (örn. "vdefault", "vcomputed", vb.).
4. Snippet tetikleyicisini yazdıktan sonra "Tab" ya da "Enter" tuşuna basarak kod parçasını tamamlayın.

## Katkıda Bulunma

Kat contributionsınızı memnuniyetle karşılıyoruz! Uygun bir şekilde yeni snippet'ler eklemek, hataları düzeltmek veya belgeleri geliştirmek için lütfen çekme istekleri oluşturun.

1. Bu projeyi kendi GitHub hesabınıza "fork"layın.
2. Yeni bir dal (branch) oluşturun: `git checkout -b my-feature-branch`
3. Değişikliklerinizi yapın ve bunları commit'leyin: `git commit -m 'Yeni snippet: dfswhile'`
4. Dalınıza (branch) it push'layın: `git push origin my-feature-branch`
5. Çekme isteği (pull request) oluşturun ve değişikliklerinizi açıklayın.

## Lisans

Bu proje, [MIT Lisansı] altında lisanslanmıştır.

---

## Snippets

| prefix                     | body                                                                                                                                                                                                                                               | description                                                                   |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| `pinia`, `cp`              | `import { createPinia } from 'pinia';`<br> `const pinia = createPinia();`<br> `app.use(pinia);`                                                                                                                                                    | **C**reate a **pinia** instance                                               |
| `pinia4vue2`, `cp4vue2`    | `import { createPinia, PiniaVuePlugin } from 'pinia';`<br> `Vue.use(PiniaVuePlugin);`<br> `const pinia = createPinia();`                                                                                                                           | **C**reate a **pinia** instance for Vue 2                                     |
| `defineStore`, `ds`        | `import { defineStore } from 'pinia';`<br> `export const useFileNameStore = defineStore('file-name', () => {`<br> `  return {`<br> `    `<br> `  }`<br> `});`                                                                                      | **D**efining **S**tores - Composing                                           |
| `defineStore`, `dso`       | `import { defineStore } from 'pinia';`<br> `export const useFileNameStore = defineStore('file-name', {`<br> `  state: () => ({`<br> `    `<br> `  }),`<br> `  getters: {`<br> `    `<br> `  },`<br> `  actions: {`<br> `    `<br> `  },`<br> `});` | **D**efining **S**tores - **O**ption                                          |
| `ims`                      | `import { useFeatureStore } from '@/stores/feature';`<br> `const featureStore = useFeatureStore();`S                                                                                                                                               | **Im**port **S**tore                                                          |
| `imstr`                    | `import { storeToRefs } from 'pinia';`<br> `const { properties } = storeToRefs(store);`                                                                                                                                                            | **Im**port **s**tore**T**o**R**efs()                                          |
| `imms`                     | `import { mapState } from 'pinia';`<br> `...mapState(useFeatureStore, ['state/getter']),`                                                                                                                                                          | **Im**port **m**ap**S**tate                                                   |
| `imma`                     | `import { mapActions } from 'pinia';`<br> `...mapActions(useFeatureStore, ['actions']),`                                                                                                                                                           | **Im**port **m**ap**A**ctions                                                 |
| `immws`                    | `import { mapWritableState } from 'pinia';`<br>`...mapWritableState(useFeatureStore, ['state/getter']),`                                                                                                                                           | **Im**port **m**ap**W**ritable**S**tate                                       |
| `ms`                       | `...mapState(useFeatureStore, ['state/getter']),`                                                                                                                                                                                                  | Usage with the Options API - Without setup() - **m**ap**S**tate()             |
| `ma`                       | `...mapActions(useFeatureStore, ['actions']),`                                                                                                                                                                                                     | Usage with the Options API - Without setup() - **m**ap**A**ctions()           |
| `mws`                      | `...mapWritableState(useFeatureStore, ['state/getter']),`                                                                                                                                                                                          | Usage with the Options API - Without setup() - **m**ap**W**ritable**S**tate() |
| `store.$patch`, `sp`       | `featureStore.$patch((state) => {`<br> `  `<br> `});`                                                                                                                                                                                              | Mutating the state: **s**tore.$**p**atch                                      |
| `store.$subscribe`, `ss`   | `featureStore.$subscribe((mutation, state) => {`<br> `  `<br> `});`                                                                                                                                                                                | Subscribing to state: **s**tore.$**s**ubscribe                                |
| `store.$onAction`, `sa`    | `const unsubscribe = featureStore.$onAction(`<br> `  ({ name, store, args, after, onError }) => {`<br> `    `<br> `    after((result) => { });`<br> `    onError((error) => { });`<br> `  }`<br> `);`                                              | Subscribing to actions: **s**tore.$**o**nAction                               |
| `store2composition `, `us` | `const featureStore = useFeatureStore();`                                                                                                                                                                                                          | Store @ Composition API, **u**seFeature**S**tore                              |
| `store2option`, `uso`      | `setup() {`<br> `  const featureStore = useFeatureStore()`<br> `  return { featureStore }`<br> `},`                                                                                                                                                | Store @ Options API, **u**seFeature**S**tore     
