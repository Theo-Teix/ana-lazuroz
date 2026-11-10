# Ana Lazuroz, Nutricionista

Página da nutricionista clínica e esportiva Ana Lazuroz (@analazuroznutri), que atende mulheres 35+ em Salto e Indaiatuba, SP. Ela não tinha site; esta é a primeira versão, feita do zero.
Versão 4 (09/11/2026), conceito "a pista": abertura escura com a foto dela numa moldura de pista de corrida, seletor de temas que muda a mensagem do WhatsApp, rotina em mosaico, avaliações em esteira, planos como percurso (largada, 90 dias, chegada) e mapa do consultório.
HTML, CSS e JavaScript puros, sem build. Todos os botões de agendamento abrem o WhatsApp.

## Estrutura

```
index.html                 página completa (estilos e scripts dentro do arquivo)
img/ana-hero.jpg           foto da abertura (à mesa do consultório, perfil do Google)
img/ana-sorriso.jpg        tema Climatério
img/ana-suco.jpg           tema Intestino
img/ana-adipometro.jpg     tema Emagrecimento (jaleco e adipômetro, perfil do Google)
img/ana-espelho.jpg        tema Massa muscular
img/ana-prova.jpg          tema Desempenho (chegada de prova)
img/ana-corrida.jpg        rotina: treino
img/ana-feira.jpg          rotina: feira
img/ana-cappuccino.jpg     rotina: cappuccino proteico
img/ana-leitura.jpg        rotina: leitura
img/instituto.jpg          fachada do Instituto Saúde em Movimento (perfil do Google)
img/ana-mesa.jpg           foto da seção final (perfil do Google)
img/favicon.png            ícone da aba
img/apple-touch-icon.png   ícone ao salvar na tela do celular
vercel.json                configuração da Vercel (URLs limpas)
```

## Publicar

1. Crie um repositório no GitHub (ex.: `Ana_Lazuroz`) e envie os arquivos desta pasta para a raiz dele.
   Importante: **arraste a pasta `img` inteira** para a área de upload. O botão "choose your files" não envia pastas.
2. Na Vercel, clique em **Add New → Project**, importe o repositório e mantenha:
   - Project Name: `nutri-analazuroz`
   - Framework Preset: **Other**
   - Build Command: vazio
   - Output Directory: vazio (raiz)
3. Clique em **Deploy**. O site fica em https://nutri-analazuroz.vercel.app/ e cada novo commit publica a atualização sozinho.

## Imagens

Ao trocar uma imagem mantendo o mesmo nome, aumente o número `?v=1` nos links do `index.html` (por exemplo `?v=2`) para os navegadores baixarem a versão nova.
As fotos do Instagram são de qualidade média (ampliadas). Se a Ana mandar fotos originais, basta substituir os arquivos com o mesmo nome. Os prompts para gerar uma foto de abertura por IA (autorizada pela cliente) estão em `previas/ana-lazuroz/prompts-gemini.md`.

## Editar conteúdo

- Número do WhatsApp: variável `numero` no fim do `index.html` (hoje 5511939468632) e o número exibido no balão final e no rodapé.
- Mensagens automáticas: atributo `data-wa` de cada botão. Ao escolher um tema, todas viram "Olá, Ana! Vim pelo site e quero começar pelo <tema>." (objeto `TEMAS` no script).
- Temas: cada um é um `<article class="painel">` com id próprio (`#climaterio`, `#intestino`, `#emagrecimento`, `#massa-muscular`, `#desempenho`). Links com esses endereços já abrem o tema escolhido.
- Horários: lista `.horarios` e a regra do "Aberto agora" no fim do script (seg a qui 8h às 19h, sex 8h às 18h).
- Cores: variáveis no início do `<style>` (`--cafe`, `--leite`, `--aveia`, `--folha`, `--coral`, `--pessego`).
- Se o endereço final do site mudar, atualize `og:url`, `og:image` e `canonical` no `<head>`.

## A confirmar com a cliente

- Se trabalha com consulta avulsa e acompanhamentos de 90 e 180 dias.
- CRN (não aparece no site porque não está publicado).
- Endereço em Indaiatuba (a bio cita a cidade, mas sem endereço).
- Parceria com a Academia Corpo São, citada no tema Massa muscular.
