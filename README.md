# Yasmin Almeida — Portfolio Website

Site de portfólio pessoal, exportado de uma sessão de design no Claude ("Doc Canvas") e mantido como site estático auto-contido.

## Estrutura

```
index.html          # Página principal (export "standalone" do Claude Doc Canvas)
support.js          # Runtime de renderização (dc-runtime) — necessário para os bindings {{ }} do index.html
image-slot.js        # Componente de slots de imagem/vídeo usado no layout
browser-window.jsx  # Componente de mockup de janela de navegador (usado nas seções de projetos web)
ios-frame.jsx        # Componente de mockup de dispositivo iOS (usado nas seções mobile)
assets/              # Imagens e vídeos usados no site (versionados via Git LFS)
```

## Rodando localmente

Como é um site estático, basta servir a pasta com qualquer servidor HTTP simples, por exemplo:

```bash
npx serve .
```

Abrir `index.html` diretamente via `file://` pode não funcionar corretamente por causa do carregamento de módulos/scripts — prefira servir via HTTP.

## Notas

- Requer Git LFS (`git lfs install`) para clonar corretamente as imagens/vídeos em `assets/`.
- Os arquivos `.dc.html` (versões editáveis no Claude) e a pasta `uploads/` do export original não foram incluídos — continham apenas material de referência/duplicado, não usado na página final.
- Vídeos usam as versões `-lite.webm` (mais leves) ao invés das versões `.mp4` originais, que também não foram incluídas.
