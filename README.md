# Agenda de Tarefas by Center Soft Inc.®

Central local para acesso e gerenciamento de uma agenda de tarefas diretamente no navegador.

## Sobre o projeto

A **Agenda de Tarefas** é uma interface web que centraliza o acesso ao módulo `Agenda de Tarefas.html`. O conteúdo do módulo é carregado dentro da página principal por meio de um `iframe`, mantendo a navegação em uma única tela.

O projeto possui tema escuro com detalhes dourados, tela inicial, menu lateral, configuração de senha, bloqueio manual e uma política integrada de uso e backup dos dados.

## Funcionalidades

- Tela inicial da Agenda de Tarefas.
- Acesso ao módulo por menu lateral.
- Carregamento do módulo em `iframe`.
- Controle de acesso por senha local.
- Alteração ou remoção da senha nas configurações.
- Bloqueio manual da interface.
- Persistência da senha com `localStorage`.
- Modal com política de uso, backup e isenção de responsabilidade.
- Interface em português do Brasil.

## Módulo disponível

| Módulo | Arquivo | Acesso |
|---|---|---|
| Agenda de Tarefas | `Agenda de Tarefas.html` | Botão com ícone de relógio no menu lateral |

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript Vanilla
- `localStorage`
- `iframe`
- Google Fonts: Cinzel e Montserrat

## Estrutura sugerida

```text
agenda-de-tarefas/
├── index.html
├── icon.ico
└── Agenda de Tarefas.html
```

> Mantenha o nome `Agenda de Tarefas.html` exatamente como definido no `index.html`, incluindo espaços e letras maiúsculas.

## Como executar

1. Coloque o `index.html`, o `icon.ico` e o arquivo `Agenda de Tarefas.html` na mesma pasta.
2. Abra o `index.html` em um navegador moderno.
3. Clique no ícone de relógio no menu lateral para abrir a agenda.
4. Use o ícone de engrenagem para acessar as configurações de segurança.
5. Use o ícone de cadeado para bloquear a aplicação.

## Controle de acesso

A senha é mantida na chave `senhaMaster` do `localStorage`. Se nenhuma senha tiver sido gravada anteriormente, o sistema utiliza uma senha vazia.

A senha pode ser alterada nas configurações. Ao deixar o campo da nova senha vazio, a proteção por senha é removida.

> Esse controle é executado inteiramente no navegador. Ele funciona como uma barreira local de conveniência e não substitui autenticação em servidor, criptografia ou gerenciamento de usuários.

## Armazenamento e backup

O sistema informa que os dados são armazenados localmente na memória do navegador, sem servidor externo ou banco de dados em nuvem para sincronização.

A realização de backups periódicos é responsabilidade do usuário. Recomenda-se utilizar as funções de exportação ou backup disponíveis no módulo e guardar as cópias em um local seguro.

A limpeza dos dados do navegador, a formatação do dispositivo, falhas do sistema operacional, ações de antivírus e a ausência de backups podem causar perda, corrupção ou exclusão das informações.

## Personalização visual

As cores principais são controladas por variáveis CSS:

```css
:root {
    --bg-deep: #060b1a;
    --accent: #d4af37;
    --border: rgba(255, 255, 255, 0.08);
}
```

A imagem de fundo é definida na classe `.fundo-background`. As fontes Cinzel e Montserrat são carregadas pelo Google Fonts.

## Compatibilidade

Use um navegador moderno com JavaScript e `localStorage` habilitados.

Como a imagem de fundo e as fontes são carregadas de serviços externos, esses elementos podem não aparecer quando o computador estiver sem acesso à internet.

## Observações técnicas

- O `login-overlay` inicia oculto por estilo inline.
- O módulo é aberto pela função `openModule()`.
- O retorno à tela principal é controlado pela função `goHome()`.
- A função `fazerLogout()` exibe a tela de login e bloqueia os itens normais do menu.
- As configurações e a política de backup são apresentadas em modais independentes.

---

### Instalação no computador

### No Google Chrome ou Microsoft Edge:

  1. Abra o endereço publicado do projeto.
  2. Aguarde o carregamento completo da página.
  3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
  4. Selecione Instalar aplicativo ou Instalar este site como aplicativo.
  5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

### Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione Instalar aplicativo ou Adicionar à tela inicial.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

**Observações**

A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
Abrir somente o arquivo index.html pelo computador não garante a instalação como PWA.
O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
O funcionamento offline depende da configuração do service-worker.js e dos arquivos adicionados ao cache.
Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

---

## Autor

**Alberto de Campos Neto**

**Center Soft Inc.®**

## Licença

Todos os direitos reservados. Os termos específicos de uso, cópia, alteração e distribuição devem ser definidos pelo proprietário do projeto.

## Aviso

> Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.

