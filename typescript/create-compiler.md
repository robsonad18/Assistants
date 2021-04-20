# Criar compilador
 - Criar compilador do typescript
 - Ter node js instalado para conseguir usar o npm
 - Rodar npm init no seu projeto
 - Ele ira criar o arquivo package.json
 - Rodar npm install typescript@2.3.2 --save-dev
 - Ele foi adicionado as dependencias do arquivo package.json
 - A pasta node_modules foi criada, dentro de typescript/bin/tsc vai estar o compilador do typescript
 - Crie o arquivo tsconfig.json, nele fica toda a configuração do compilador
 - Dentro do arquivo cole isso, essa é a configuração minima:
{
    "compilerOptions": {
        "target": "es6",
        "outDir": "app/js"
    },
    "include": [
        "app/ts/**/*"
    ]
}

 - target: Indica para qual versão do ecmascript o seu codigo deve ser traduzido
 - include: indica quais arquivos o compilador tem que levar em consideração na hora que for compilar
 - outDir: o resultado da compilação ira cair dentro da pasta indicada nesse indice
 - Abra o arquivo package.json, dentro da chave script, crie o indice compile e adicione o valor tsc que é referente ao compilador typescript
