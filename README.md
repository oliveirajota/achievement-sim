# Simulador de Conquistas

Gera a animação de "conquista desbloqueada" nos estilos Xbox, PlayStation e Steam, com som, para usar ao vivo no OBS ou exportar como vídeo.

**Online:** https://achievement.easypress.app

![estilos](https://img.shields.io/badge/estilos-Xbox%20%7C%20PlayStation%20%7C%20Steam-555)

## O que faz
- Texto, cabeçalho, pontos (G), tipo de troféu, descrição e ícone personalizáveis.
- Sons sintetizados para cada estilo, ou um arquivo de áudio seu.
- Fundo transparente, preto, verde (chroma key) ou cor livre.
- Resoluções 16:9 (720p, 1080p, 1440p), vertical 9:16 e quadrada.
- **Exportação de vídeo** (MP4 ou WebM). Por padrão exporta só a área da conquista; também pode exportar a tela inteira. WebM mantém a transparência.
- **Modo OBS:** um link com todos os parâmetros para usar numa fonte Navegador. A animação toca quando a fonte fica visível.

## Como funciona
É um único arquivo `index.html`, sem dependências e sem backend. Animação (canvas 2D), som (Web Audio) e gravação (MediaRecorder) rodam no navegador. Nada é enviado ao servidor.

Testado no Chrome/Chromium. O Firefox deve gravar apenas WebM.

## Uso local
Abra o `index.html` no navegador. No OBS, use o botão **Copiar link do OBS** e cole o link numa fonte **Navegador**, com "Arquivo local" desmarcado. As instruções completas estão na própria página.

## Aviso
Projeto independente e não oficial, sem afiliação com Microsoft (Xbox), Sony (PlayStation) ou Valve (Steam). As marcas pertencem aos respectivos donos. Nenhum áudio ou logotipo oficial é distribuído; os sons são sintetizados.
