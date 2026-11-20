<p align="center">
  <img src="images/TOOLS_GITHUB_ACTIONS_MONITOR_WATCH_BANNER.svg" alt="TOOLS-GITHUB-ACTIONS-MONITOR-WATCH banner" width="100%">
</p>

# 🛠️ TOOLS-GITHUB-ACTIONS-MONITOR-WATCH

<p align="center"><a href="README.md">🇺🇸 English</a> | <a href="README_spa.md">🇪🇸 Español</a> | <a href="README_fra.md">🇫🇷 Français</a> | <a href="README_ita.md">🇮🇹 Italiano</a> | <a href="README_deu.md">🇩🇪 Deutsch</a> | <a href="README_zho.md">🇨🇳 中文</a> | <a href="README_jpn.md">🇯🇵 日本語</a> | 🇵🇹 <b>Português</b></p>

### Versão mínima prevista para relógio com Wear OS da aplicação Android do GitHub Actions Monitor: uma vista rápida dos teus workflows no pulso. Apenas estrutura inicial: ainda nada está implementado.

<p align="center">
  <img src="https://img.shields.io/badge/License-GPL%203.0--or--later-blue.svg" alt="GPL 3.0 or later">
  <img src="https://img.shields.io/badge/Stack-Kotlin%20%2B%20Wear%20OS%20(planned)-blue.svg" alt="Kotlin and Wear OS (planned)">
  <img src="https://img.shields.io/badge/Languages-8-00E5FF.svg" alt="Languages">
  <img src="https://img.shields.io/badge/Tests-none%20yet-lightgrey.svg" alt="Tests">
  <img src="https://img.shields.io/badge/Version-0.0.1-0f6cbd.svg" alt="Version">
  <img src="https://img.shields.io/badge/Maturity-scaffolding-FFB020.svg" alt="Maturity">
</p>

---

**Verificação de honestidade - o que corre hoje:** nada da aplicação de relógio. Este repositório contém apenas a sua base: os documentos, o manifesto, a licença e as verificações partilhadas do repositório. Não há código, nem pacote, nem ecrã, nem serviço de notificações, nem testes da aplicação, e nada foi experimentado num relógio.

---

## 📋 Num relance

| | |
|---|---|
| Versão | `0.0.1` |
| Maturidade | Estrutura inicial |
| Testes | Nenhum por enquanto (apenas as verificações do repositório) |
| Tecnologias | Kotlin e Wear OS (previsto) |
| Em hardware real | Nunca executada num relógio |

**Ir para:** [Visão geral](#-visão-geral) · [Arquitetura](#-arquitetura) · [Início rápido](#-início-rápido) · [Testes](#-testes) · [Estrutura do repositório](#-estrutura-do-repositório) · [Projetos relacionados](#-projetos-relacionados)

## 🚦 Estado do projeto

Cada linha é uma parte deste repositório e a luz diz até onde chega hoje. É escrita com o que o repositório consegue demonstrar (testes, compilações, execuções), não com o que está previsto.

🟢 Feito e verificado · 🟡 Funciona, com limites conhecidos · 🟠 Feito a meio ou ainda por verificar · 🔴 Por fazer ou a não funcionar

| Área | Estado | O que significa aqui |
|---|---|---|
| Base do repositório | 🟡 | O manifesto, os README em oito idiomas, a licença e as verificações partilhadas do repositório correm no CI. |
| Código da aplicação de relógio | 🔴 | Por começar: este repositório ainda não tem nenhum projeto de relógio. |
| Testes | 🔴 | A aplicação não tem testes; só correm as verificações do repositório. |
| Ligação ao monitor | 🔴 | Por começar. Ainda não está decidido como o relógio obterá os dados (através da aplicação Android ou diretamente). |
| Relógio e notificações | 🔴 | Por começar e nunca executada num relógio; nenhum serviço de notificações está ligado. |

## 🎯 Visão geral

* **O que será:** uma versão mínima para relógio com Wear OS da aplicação Android, com uma vista rápida para saber se algo está a vermelho e dos últimos alertas importantes do teu próprio monitor.
* **Segue a aplicação Android:** é construída depois de [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID) e limita-se a um subconjunto do que essa aplicação mostra.
* **Só leitura:** só lerá do teu monitor. Não escreverá no GitHub nem alterará nada no monitor.
* **O que não é (ainda):** não há aplicação para instalar, nem release, nem data. Este repositório apenas reserva o seu lugar e diz com honestidade o que está previsto.

## 🧩 Papel no EH3D

TOOLS-GITHUB-ACTIONS-MONITOR-WATCH pretende ser a versão mínima para relógio com Wear OS da aplicação Android [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID) do GitHub Actions Monitor ([TOOLS-GITHUB-ACTIONS-MONITOR](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR)). Mostraria uma pequena parte do que o monitor já sabe e não decidiria nada por si.

## 🏛️ Arquitetura

<p align="center">
  <img src="images/architecture.svg" alt="Arquitetura de TOOLS-GITHUB-ACTIONS-MONITOR-WATCH: quem o usa, o que contém e de que depende" width="100%">
</p>

Como as partes deste repositório se encaixam: quem o usa, o que contém e de que depende. A imagem é desenhada a partir de `docs/architecture.json` e verificada com o código.

## ✨ Funcionalidades

**Previsto, e nada disto existe ainda:**
* Uma vista rápida: há algo a vermelho?
* Os últimos alertas importantes de forma breve.
* Opcionalmente, uma vibração perante um alerta importante, desativada por predefinição.
* Textos em oito idiomas.

**Não previsto:** escrever no GitHub, listas longas ou qualquer ação que não seja olhar. O relógio não será necessário para executar o monitor.

## 🔒 Segurança e proteção

* Previsto: a aplicação de relógio só lê, e qualquer token de acesso fica nos teus dispositivos e é enviado apenas para o endereço do teu monitor (ou para a aplicação Android).
* Nada de secreto tem lugar neste repositório: nem chaves, nem tokens, nem ficheiros de serviços de notificações, nem chaves de assinatura.
* São intenções de conceção. Nada disto existe ainda, pelo que ninguém o pôde rever.

## 🚀 Início rápido

Ainda não há nada para instalar nem para executar. Para verificar a base deste repositório precisas de Python 3.10 ou posterior:

```bash
python -I tools/ci_validate.py
python -I tools/make_architecture.py --check
python -I tools/make_structure.py --check --readmes
python -I -m unittest discover -s tools -p "test_*.py"
```

## 🧪 Testes

O CI executa as verificações do repositório e os testes dessas verificações. A aplicação de relógio não tem testes próprios porque ainda não tem código, e aqui não se afirma nenhum número de testes.

## 🏗️ Compilação e publicação

Não há compilação nem release, porque não existe nenhuma versão da aplicação. A versão `0.0.1` de `VERSION`, do manifesto e do registo de alterações é a da base do repositório.

## 📂 Estrutura do repositório

<p align="center">
  <img src="images/repository-structure.svg" alt="Estrutura do repositório TOOLS-GITHUB-ACTIONS-MONITOR-WATCH" width="100%">
</p>

<details>
<summary>Versão em texto da árvore</summary>

```text
MONITOR-WATCH/
├── tools/
│   ├── ci_validate.py                           manifesto, versões, paridade dos README
│   └── make_architecture.py make_structure.py   desenham as duas imagens do README
├── docs/                                        as fontes das duas imagens
├── images/                                      banner e as duas imagens
├── .github/                                     fluxos de CI e modelos
├── VERSION                                      a versão do repositório
├── electro-hobby-3d.project.json                o manifesto do projeto
├── CHANGELOG.md                                 o que mudou em cada versão
├── SECURITY.md SUPPORT.md                       como comunicar uma vulnerabilidade e onde perguntar
└── CONTRIBUTING.md CODE_OF_CONDUCT.md LICENSE   como contribuir, o código de conduta e a licença
```

</details>

## 🗺️ Roteiro e limites conhecidos

**Limites conhecidos hoje**

* Não há código: nem aplicação, nem pacote, nem ecrã.
* Nada foi experimentado num relógio nem com um monitor real.
* O relógio segue a aplicação Android, pelo que não pode começar antes de essa aplicação existir.
* Ainda não está decidido como o relógio obtém os dados.

**A seguir**

* Esperar pela aplicação Android, decidir como o relógio obtém os dados e construir o menor ecrã útil, com os seus testes no CI.

## 🌍 Idiomas

O README e os textos existem em inglês, espanhol, francês, italiano, alemão, chinês, japonês e português europeu.

## 🔗 Projetos relacionados

* [TOOLS-GITHUB-ACTIONS-MONITOR](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR): o monitor cujos dados o relógio com Wear OS pretende mostrar
* [TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID](https://github.com/JuanenRac/TOOLS-GITHUB-ACTIONS-MONITOR-ANDROID): a aplicação Android prevista que esta versão para relógio com Wear OS segue
* [EH3D-DOCS](https://github.com/JuanenRac/EH3D-DOCS): as convenções e as verificações partilhadas

## 📚 Documentação

* [As convenções da suite](https://github.com/JuanenRac/EH3D-DOCS/blob/main/docs/CONVENTIONS.md)
* [Registo de alterações](CHANGELOG.md)

## 🤝 Contribuir e comunidade

* Antes de um pull request executa `python -I tools/ci_validate.py`; as restantes verificações correm no CI. Consulta [CONTRIBUTING.md](CONTRIBUTING.md) e o [código de conduta](CODE_OF_CONDUCT.md).
* O README existe em oito idiomas: uma alteração ao texto faz-se nos oito ficheiros, e as duas imagens são desenhadas a partir de `docs/architecture.json` e `docs/structure.json` com `tools/make_architecture.py` e `tools/make_structure.py`.
* Comunica uma vulnerabilidade em privado: [SECURITY.md](SECURITY.md). Perguntas, ideias e relatos: electrohobby3d@gmail.com ([SUPPORT.md](SUPPORT.md)).

## 👤 AUTOR

**JuanenRac (Electro Hobby 3D)** · electrohobby3d@gmail.com

## 📜 LICENÇA

Software: GPL-3.0-or-later. Ver [LICENSE](LICENSE). Os projetos de hardware da suite usam a CERN OHL-S.
