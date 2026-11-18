# ✝ Sonoplastia eJC de Lourdes v2.0

> **Painel de Controle Profissional de Sonoplastia e Efeitos Sonoros para as Peças Teatrais do eJC de Lourdes.**  
> *Execução instantânea com 1 clique • 100% Offline (PWA) • Sincronização em Nuvem (Acesse de Qualquer Lugar)*

---

## 🌟 O que há de novo na Versão 2.0?

1. **Anexo Completo de Áudios das Peças**:
   - **Upload Local**: Envie seus próprios arquivos de áudio (MP3, WAV, M4A, OGG, AAC) direto do celular ou notebook.
   - **Áudios por URL da Nuvem**: Adicione links diretos de áudios hospedados no Google Drive, Dropbox, Firebase Storage, AWS S3, etc.
   - **Gravação ao Vivo**: Grave falas de narrador, avisos ou orações com o microfone na hora.
   - **Efeitos Sonoros EJC Embutidos**: 8 efeitos teatrais pré-gerados (Sino de Igreja, Tempestade & Trovão, Suspense & Tensão, Impacto Dramático, Acorde Mariano de Oração, Vento no Deserto, Batimentos Cardíacos e Aplausos).

2. **Funcionamento 100% Offline (PWA - Progressive Web App)**:
   - Funciona mesmo no salão de retiro ou igreja sem nenhum sinal de internet ou Wi-Fi.
   - Pode ser instalado como aplicativo nativo no Android, iPhone/iPad, Windows e Mac.
   - Todos os arquivos de áudio anexados são salvos no **IndexedDB** e no **CacheStorage** local do aparelho com latência zero.
   - Indicador automático no topo: 🟢 **Online** / 🟡 **Modo Retiro (Offline 100%)**.

3. **Acesso de Qualquer Lugar (Sincronização em Nuvem)**:
   - **Suporte ao Firebase**: Conecte um projeto gratuito do Firebase (Firestore) para que qualquer membro da equipe ou coordenação veja exatamente as mesmas peças e trilhas sincronizadas em tempo real.
   - **Compartilhamento de Pacote**: Copie o código do repertório para colar no WhatsApp da equipe.
   - **Backup e Restauração em JSON**: Exporte e importe backups completos em 1 clique.

4. **Painel de Som Teatral Profissional (Soundboard)**:
   - **1 Clique para Tocar**: Disparo imediato com animação de equalizador e barra de progresso interativa (scrubbing).
   - **Botão de Pânico (PARAR TUDO)**: Interrompe todos os sons instantaneamente (tecla `Espaço`).
   - **Fade Out Suave de 3s**: Diminui a música gradualmente para não cortar abruptamente na fala dos atores (tecla `F`).
   - **Modos de Reprodução**:
     - *Solo (Tocar 1 por Vez)*: Ao disparar uma música, pausa a anterior automaticamente.
     - *Sobreposição (Mix)*: Permite tocar trilha de fundo + trovão ou efeito de sino simultaneamente.
   - **Manter Tela Ligada (Screen Wake Lock)**: Impede que o celular apague ou bloqueie a tela durante a encenação.
   - **Controle de Volume Individual por Faixa & Volume Master Geral**.

---

## 📋 Peças do eJC Pré-cadastradas

A aplicação já vem com o roteiro e efeitos de exemplo das principais peças do eJC de Lourdes:
- 🎭 **O Filho Pródigo** (A Partida, Noite de Ilusões, Queda, O Abraço do Pai)
- 🎭 **As Máscaras da Vida** (As Falsas Aparências, O Peso das Máscaras, Libertação na Cruz)
- 🎭 **O Barco e a Tempestade** (O Mar Revolto, Os Trovões, Jesus Acalma o Mar)
- 🎭 **Peça dos Pais e Família** (Conflitos, Oração Silenciosa, Reencontro e Entrada dos Pais)
- 🎭 **Consagração a Nossa Senhora de Lourdes** (Luzes Apagadas, Bênção das Velas, Envio dos Jovens)

---

## 🚀 Como Publicar no GitHub

Para colocar este projeto no seu GitHub, siga os passos abaixo no terminal:

```bash
# 1. Navegue até a pasta do projeto:
cd C:\Users\oliveira.andre\.gemini\antigravity\scratch\sonoplastia-ejc-de-lourdes

# 2. Crie um novo repositório no seu GitHub (ex: sonoplastia-ejc-de-lourdes)
# Se você tiver o GitHub CLI autenticado:
gh repo create sonoplastia-ejc-de-lourdes --public --source=. --remote=origin --push

# OU pelo método tradicional do Git:
git remote add origin https://github.com/SEU-USUARIO/sonoplastia-ejc-de-lourdes.git
git branch -M main
git push -u origin main
```

---

## ⚡ Como Publicar na Vercel

A Vercel é 100% gratuita para este tipo de projeto e atualiza automaticamente a cada commit:

### Opção 1: Pelo Painel da Vercel (Recomendado)
1. Acesse [vercel.com](https://vercel.com) e faça login com sua conta do GitHub.
2. Clique no botão **"Add New..."** > **"Project"**.
3. Selecione o repositório `sonoplastia-ejc-de-lourdes`.
4. Deixe todas as opções no padrão (Framework: *Other*, Root Directory: `./`).
5. Clique em **"Deploy"**. Em menos de 30 segundos seu link estará no ar com HTTPS e suporte a PWA!

### Opção 2: Pela Linha de Comando (Vercel CLI)
```bash
npx vercel
```

---

## ☁️ Como Configurar a Sincronização em Nuvem (Firebase Gratuito)

Para que toda a equipe acesse e sincronize as mesmas informações de qualquer celular ou computador:

1. Acesse [console.firebase.google.com](https://console.firebase.google.com/) e crie um projeto gratuito (Plano Spark).
2. No menu lateral, clique em **Criação** > **Firestore Database** e selecione "Criar banco de dados" (iniciar no modo de teste).
3. Na engrenagem de configurações do projeto (Configurações do Projeto), role até o final e clique no ícone **Web (`</>`)** para registrar o aplicativo.
4. Copie o objeto `firebaseConfig` gerado, por exemplo:
   ```json
   {
     "apiKey": "AIzaSy...",
     "authDomain": "seu-projeto.firebaseapp.com",
     "projectId": "seu-projeto",
     "storageBucket": "seu-projeto.appspot.com",
     "messagingSenderId": "123456789",
     "appId": "1:123456789:web:abcdef"
   }
   ```
5. No site da Sonoplastia, clique no ícone da **Nuvem ☁️** no cabeçalho, cole essa configuração e clique em **"Salvar & Conectar à Nuvem"**.
6. Pronto! Agora qualquer alteração feita por você ou outro equipista será salva na nuvem e baixada automaticamente no celular da sonoplastia com cache offline!

---

## ⌨️ Atalhos Rápidos de Teclado na Cabine de Som

| Tecla | Função |
| :--- | :--- |
| **Barra de Espaço** | **PARAR TUDO** instantaneamente |
| **F** | **Fade Out suave** (reduz o volume até zerar em 3 segundos) |
| **M** | **Mutar / Desmutar** o volume geral |
| **1 a 9** | Disparar os primeiros 9 áudios da peça selecionada com 1 tecla |

---

## 📱 Como Instalar no Celular (Android / iPhone)

- **Android (Chrome)**: Ao abrir o site, clique no botão **"Instalar App"** na barra superior ou clique nos 3 pontinhos do Chrome e escolha *"Instalar aplicativo"* ou *"Adicionar à tela inicial"*.
- **iPhone / iPad (Safari)**: Toque no botão de compartilhamento do Safari (quadrado com seta para cima) e selecione *"Adicionar à Tela de Início"*.

---

*Que Nossa Senhora de Lourdes interceda por todos os jovens e equipistas do eJC!* ✝
