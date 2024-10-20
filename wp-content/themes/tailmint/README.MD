Este é um tema boilerplate mínimo para WordPress usando Tailwind  [Tailwind CSS](https://tailwindcss.com/).

## Início

*   Execute `npm install`
*   Execute `npm run watch` para começar o desenvolvimento

### Geral

Você encontrará os arquivos CSS e Javascript editáveis ​​na pasta `/` src.

Antes de usar seu tema em produção, certifique-se de executar `npm run production`.


## NPM Scripts

There are several NPM scripts available. You'll find the full list in the `package.json` file under "scripts". A script is executed through the terminal by running `npm run script-name`.

Há vários scripts NPM disponíveis. Você encontrará a lista completa no arquivo `package.json` "scripts". Um script é executado através do terminal executando npm run script-name.

| Script | Descrição |
| --- | --- |
| production | Cria um build de produção (minificada) de app.js, app.css e editor-style.css. |
| dev | Cria um build de desenvolvimento de app.js, app.css e editor-style.css. |
| watch | Executa vários watch scripts simultaneamente. |


## Dicas

### Styling within the block editor

Para tornar a experiência de edição no editor de blocos mais alinhada com o estilo do front-end, um `editor-style.css` é gerado.


### CSS gerado pelo tema

CSS classes for alignment (full, wide etc.) are generated automatically. You can opt-out on this by removing the plugin from the `tailwind.config.js` file.

As classes CSS para alignment (full, wide etc.) são geradas automaticamente. Você pode optar por não fazer isso removendo o plugin do arquivo `tailwind.config.js`.


### Cores personalizadas

Várias cores e tamanhos de fonte são definidos desde o início. Você pode modificá-los em `theme.json`.


### Tradução

Para que o suporte à tradução do tema ou à string de localização funcione corretamente, você precisa gerar o arquivo .mo. Enquanto estiver na pasta do tema do idioma, execute:


```bash
    msgfmt pt_BR.po -o pt_BR.mo
   ```

## Links

*   [Tailwind CSS Documentation](https://tailwindcss.com/docs)
*   [Laravel Mix Documentation](https://laravel-mix.com)
*   [Esbuild Documentation](https://esbuild.github.io)

## Author

*   [Denis Almeida](https://denisalmeida.com)
