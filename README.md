# goup - Gerenciador Completo para Go

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Bash](https://img.shields.io/badge/Made%20with-Bash-1f425f.svg)](https://www.gnu.org/software/bash/)

**goup** é uma ferramenta completa para instalar, gerenciar e manter o ambiente Go (Golang) em sistemas Linux. Projetada para ser simples, robusta e completa, oferecendo tudo que um desenvolvedor Go precisa em um único script.

## ✨ Características

- 🚀 **Instalação automática** do Go diretamente da fonte oficial
- 🔄 **Gerenciamento de múltiplas versões** com sistema organizado
- 🛠️ **Instalação automática de ferramentas essenciais** (linters, debuggers, etc.)
- 🎯 **Auto-instalação** como comando global do sistema
- ✅ **Verificações rigorosas** e testes automatizados
- 📝 **Logs detalhados** para depuração
- 🐧 **Compatível** com qualquer distribuição Linux
- 🎨 **Interface amigável** com ajuda contextual

## 📦 Instalação Rápida

```bash
# Baixe o script
curl -fsSL https://raw.githubusercontent.com/helton-godoy/goup/main/goup -o goup
chmod +x goup

# Instale Go + ferramentas essenciais + goup globalmente
./goup --install-tools --self-install
```

Pronto! Agora você tem Go completamente configurado e pode usar `goup` de qualquer lugar.

## 🎮 Uso

### Instalação Básica

```bash
# Instalar versão mais recente
goup

# Instalar versão específica
goup --version go1.21.5

# Instalar com ferramentas essenciais
goup --install-tools
```

### Gerenciamento de Versões

```bash
# Listar versões instaladas
goup --list

# Alternar versão padrão
goup --switch go1.21.5

# Atualizar ferramentas
goup --update-tools
```

### Instalação do goup

```bash
# Auto-instalar como comando global
goup --self-install

# Ou instalar manualmente
sudo cp goup /usr/local/bin/goup
sudo chmod +x /usr/local/bin/goup
```

## 🏗️ Estrutura de Instalação

```
/usr/local/
├── bin/goup                    # Comando goup
├── go -> .go-versions/go1.25.3/ # Versão padrão (symlink)
└── .go-versions/
    ├── go1.21.5/               # Versão específica
    │   ├── bin/
    │   │   ├── go
    │   │   ├── gofmt
    │   │   ├── goimports
    │   │   ├── staticcheck
    │   │   ├── air
    │   │   ├── dlv
    │   │   └── golangci-lint
    └── go1.25.3/               # Outra versão
```

## 🛠️ Ferramentas Incluídas

Quando usa `--install-tools`, o goup instala automaticamente:

- **`goimports`** - Formatação automática de imports
- **`staticcheck`** - Linter avançado para código Go
- **`air`** - Hot reload para desenvolvimento web
- **`dlv`** - Debugger oficial do Go
- **`golangci-lint`** - Linter completo com múltiplas regras

## 📋 Requisitos

- Linux (qualquer distribuição)
- `curl`, `tar`, `grep`, `uname`, `sha256sum`
- Permissões de escrita em `/usr/local/` (ou use `--install-dir`)

## 🔧 Opções Avançadas

```bash
goup --help                    # Ver todas as opções
goup --install-dir /opt/go     # Instalar em diretório customizado
goup --version go1.20.0        # Instalar versão específica
```

## 🤝 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para:

- Reportar bugs
- Sugerir novas funcionalidades
- Enviar pull requests
- Melhorar a documentação

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

## 🙏 Agradecimentos

- [Go Team](https://golang.org/) pela linguagem incrível
- Comunidade Go por todas as ferramentas e bibliotecas
- Todos os contribuidores que tornam o ecossistema Go tão rico

---

**goup** - Simplificando o desenvolvimento Go desde o primeiro `go version`! 🚀
