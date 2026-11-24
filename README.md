# Simulador de Conquistas

Gera animações de conquista desbloqueada para usar ao vivo no OBS ou exportar como vídeo ou GIF. A interface está disponível em português do Brasil e inglês dos EUA.

**Online:** https://achievement.easypress.app

## Estilos

- Xbox, PlayStation e Steam.
- Aventura em Blocos, inspirado nos avanços do Minecraft, com variações de avanço, meta e desafio.
- Emblema, inspirado na linguagem visual dos jogos da Nintendo.
- Arcade Retrô, com placar e som 8-bit.
- Jogos Mobile, com cartão compacto para vídeos verticais.

## O que faz
- Texto, cabeçalho, pontos (G), tipo de troféu e descrição personalizáveis.
- Sons sintetizados para cada estilo, ou um arquivo de áudio seu.
- Fundo transparente, preto, verde (chroma key) ou cor livre.
- Resoluções 16:9 (720p, 1080p, 1440p), vertical 9:16 e quadrada.
- **Exportação de vídeo** (MP4 ou WebM). Por padrão exporta só a área da conquista; também pode exportar a tela inteira. WebM mantém a transparência.
- **GIF animado** em recorte ou tela inteira, com repetição contínua. O GIF é silencioso, é exportado a 20 quadros por segundo e tem até 960 pixels no lado maior. Com fundo transparente, cada pixel fica transparente ou opaco.
- **Modo OBS:** um link com os parâmetros e o idioma para usar numa fonte Navegador. A animação toca quando a fonte fica visível.

## Como funciona
É um único arquivo `index.html`, sem dependências e sem backend. A animação, o som e a exportação de vídeo e GIF rodam no navegador. Nada é enviado ao servidor.

Testado no Chrome/Chromium. O Firefox deve gravar apenas WebM.

## Uso local
Abra o `index.html` no navegador. No OBS, use o botão **Copiar link do OBS** e cole o link numa fonte **Navegador**, com "Arquivo local" desmarcado. As instruções completas estão na própria página.

## Personalizar a URL do OBS

A fonte dispara a animação ao carregar a página com `obs=1`. Use `st` para o estilo, `title` para o nome ou mensagem, `head` para o cabeçalho e `lang` para o idioma dos textos padrão. O botão **Copiar link do OBS** gera a URL com as configurações escolhidas no painel.

```js
const url = new URL('https://achievement.easypress.app/');
url.search = new URLSearchParams({
  obs: '1',
  st: 'ps',
  title: 'João & Luísa',
  head: 'Inscrito no canal!',
  lang: 'pt-BR',
  res: '1080',
});
// Configure a fonte Navegador com url.href.
```

Uma automação que recebe eventos da live pode montar essa URL a cada inscrição, comando ou mensagem selecionada e atualizar a fonte com [Set Browser Source URL](https://docs.streamer.bot/api/sub-actions/obs-studio/sources/set-browser-source-url).

Use o parâmetro `icon` para personalizar a imagem do overlay com uma URL ou um caminho acessível à fonte Navegador do OBS. O editor usa os ícones padrão de cada estilo.

## Aviso
Projeto independente e não oficial, sem afiliação com as marcas citadas. As marcas pertencem aos respectivos donos. Os sons são sintetizados.
