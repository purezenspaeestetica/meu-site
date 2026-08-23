# Purezen Spa & Estética — site

Site institucional de página única. HTML estático, sem build: o navegador
abre o `index.html` direto. Tailwind, GSAP e os ícones Lucide vêm por CDN.

## Estrutura

```
index.html          o site inteiro (marcação, estilos e scripts)
fotos/              fotografias
  *.webp            versões otimizadas — são estas que o site usa
  *.png *.jpg       originais em alta, guardados como arquivo-mestre
artes/              artes de divulgação dos serviços (não usadas pelo site)
.vercelignore       mantém os originais e as artes fora do deploy
```

Os originais ficam versionados para que nada dependa da máquina de uma
pessoa só, mas não são publicados: o site carrega apenas os `.webp`.

## Rodar localmente

```bash
python -m http.server 8000
```

Depois abra `http://localhost:8000`.

## Publicar

O deploy é automático: todo `git push` na branch `main` publica.

Para trocar uma foto, gere o `.webp` a partir do original e ajuste no
`index.html` o `src` e os atributos `width`/`height` para as dimensões
reais da imagem nova. Sem isso a página dá um salto durante o
carregamento, porque o navegador reserva o espaço na proporção errada.

## Contato do negócio

WhatsApp e telefone: (11) 99205-1143
Rua Henrique Bernardelli 136, Santana, São Paulo
Seg a sex 10h-18h, sáb 10h-16h
