Eterium Launcher
Launcher de Minecraft desktop desenvolvido com Electron + React + TypeScript.

Stack
Electron
React 18
TypeScript
Vite
Tailwind CSS + shadcn/ui
XMCL (@xmcl/core, @xmcl/installer, @xmcl/user, @xmcl/curseforge)
Funcionalidades principais
Instalação e verificação de instância Minecraft (vanilla + loader + modpack)
Fluxo CurseForge com cache/aplicação e progresso
Configurações de launcher e Minecraft
Integração com bandeja do sistema (tray)
Build para Windows via electron-builder
Requisitos
Node.js 20+
npm 10+
Windows (build principal configurado para Windows)
Como rodar em desenvolvimento
npm install
npm run electron:dev
Scripts úteis
npm run dev: inicia apenas o frontend Vite
npm run electron:dev: inicia Vite + Electron (modo desenvolvimento)
npm run build: build do frontend
npm run dist: gera instalador/app com electron-builder
npm run electron:build: build frontend + empacotamento
npm run electron:publish: build + publicação configurada no build.publish
Build e distribuição
As configurações de empacotamento ficam em package.json, no bloco build:

Target Windows: nsis-web
Idioma do instalador: pt_BR
Publicação: GitHub Releases (repo de distribuição)
Artefatos são gerados na pasta release/.

Estrutura (resumo)
src/: interface React e lógica do renderer
electron/: processo principal, preload e integrações nativas
public/: assets estáticos
Observações
Para publicar instaladores, use o fluxo de releases do GitHub configurado no electron-builder.
