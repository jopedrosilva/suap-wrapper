# suap-wrapper [![npm version](https://badge.fury.io/js/suap-wrapper.svg)](https://badge.fury.io/js/suap-wrapper)

Wrapper escrito em JavaScript para acessar a [API](https://suap.ifrn.edu.br/api/docs) do __Sistema Unificado de Administração Pública (SUAP)__.

## Usando

O __suap-wrapper__ está disponibilizado através do __npm__ (gerenciado de pacotes para Node.js), então:

```shell
npm install --save suap-wrapper
```

Após isso, você já pode usar o __suap-wrapper__ no seu projeto:

```javascript
'use strict';

import Suap from 'suap';

let autenticar = Suap.autenticar('201610140400xx', 'm1nhasenh4');

if (autenticar) {
  autenticar.then((response) => {
    console.log(`Seu token é: <${response.data.token}>.`);
  }, (error) => {
    console.log('Falha na autenticação.')
  });
}
```

## Ajudar no desenvolvimento

Estas instruções orientarão você sobre como ajudar no desenvolvimento do projeto.

### Requisitos

Você precisar ter o [Node.js](https://nodejs.org/en/) instalado em sua máquina. Após instalar, verifique se `node` e `npm` estão no seu _path_:

```shell
node --version
npm --version
```

### Instalando

Fork e clone o repositório, depois peça para o `npm` instalar as dependências:

```shell
git clone https://github.com/seu-usuario/suap-wrapper.git
cd suap-wrapper
npm install
```

Após estes comandos, você deve ter na sua pasta:

```
├── index.js
├── LICENSE
├── node_modules
│   └── axios
├── package.json
└── README.md
```

Agora é só olhar a documentação da [API](https://suap.ifrn.edu.br/api/docs) do SUAP e adicionar novas funcionalidades.

## Feito com...

- [Axios](https://github.com/mzabriskie/axios)

## Contribuição

Ficaremos muito felizes se você contribuir com este projeto seja enviando _Pull Request_ ou notificando bugs pelas _Issues_.

## Versionamento

Estamos usando o [SemVer](http://semver.org/) para versionamento. Para ver as versões disponíveis: [tags deste repositório](https://github.com/Projeto-SIAC/suap-wrapper/tags). 

## Autores

* **Felipe Pontes** - *Trabalho inicial* - [felipemfp](https://github.com/felipemfp)

Veja também a lista de [contribuidores](https://github.com/Projeto-SIAC/suap-wrapper/contributors) que participaram deste projeto.

## Licença

Este projeto é licenciado pela Licença MIT - veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.