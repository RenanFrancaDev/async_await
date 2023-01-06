# Requisição de API .then para async await

```
const Api = {}

Api.getExamplesArr = (offset, limit, ...) => {
const url = `https://websiteaddress/api/v2/examples?offset=${offset}&limit=${limit}`
return fetch(url)
    .then((response) => response.json())
    .then((jsonBody) => jsonBody.results)
    .then((examplesArr) => examplesArr.map((example) => example.getExamplesDetail(examples))) => requisição de API dentro de outra API
    .then((detailRequest) => Promise.all(detailRequest))
    .then((examplesDetails) => examplesDetails)
    .catch((error) => console.error('error'))

}

Api.getDetail = (example) => {
    return fetch(example.url)
    .then((response) => response.json())
    .then((example) => convertApiDetailtoExample(example))
                            
}

function convertApiDetailtoExample(detail){

    const variavel = new Obj();
    variavel.number = detail.id;
    variavel.name = detail.name;
    variavel.types = detail.types.map((typeSlot) => typeSlot.type.name); (se houver um array)
    variavel.type = variavel.types[0]; (se houver um array)
    variavel.photo = detail.sprites.other.dream_world.front_default;
    variavel.weight = detail.weight;
    variavel.height = detail.height;
   
  
    return variavel
}

```

```
const Api = {}

Api.getExamplesArr = (offset, limit, ...) => {
const url = `https://websiteaddress/api/v2/examples?offset=${offset}&limit=${limit}`
return fetch(url)
    .then((response) => response.json())
    .then((jsonBody) => jsonBody.results)
    .then((examplesArr) => examplesArr.map((example) => example.getExamplesDetail(examples))) => requisição de API dentro de outra API
    .then((detailRequest) => Promise.all(detailRequest))
    .then((examplesDetails) => examplesDetails)
    .catch((error) => console.error('error'))

}

Api.getDetail = (example) => {
    return fetch(example.url)
    .then((response) => response.json())
    .then((example) => convertApiDetailtoExample(example))
                            
}

function convertApiDetailtoExample(detail){

    const variavel = new Obj();
    variavel.number = detail.id;
    variavel.name = detail.name;
    variavel.types = detail.types.map((typeSlot) => typeSlot.type.name); (se houver um array)
    variavel.type = variavel.types[0]; (se houver um array)
    variavel.photo = detail.sprites.other.dream_world.front_default;
    variavel.weight = detail.weight;
    variavel.height = detail.height;
   
  
    return variavel
}
```



