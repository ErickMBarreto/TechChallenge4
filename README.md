# Análise de Expressões Faciais em Vídeo

## Descrição

Projeto de análise de vídeo e realizar reconhecimento facial, detecção de emoções, identificação de atividades e geração de relatórios automatizados. O projeto utiliza técnicas de visão computacional e aprendizado de máquina.

---

## Índice

1. [Descrição](#descrição)
2. [Ações Implementadas](#ações-implementadas)
3. [Pré-requisitos](#pré-requisitos)
4. [Instalação](#instalação)
5. [Como Executar](#como-executar)

---

## Ações Implementadas

### Vídeo Anotado
- Geração de vídeo de saída com todas as anotações
- Caixas delimitadoras ao redor de rostos
- Rótulos de emoção com confiança
- Informação de atividade no canto superior
- Contador de frames e rostos detectados
- Geração de relatório consolidado no final da execução

## Pré-requisitos

- **Python**: 3.12 ou superior (obrigatório)
- **uv**: Gerenciador de pacotes Python (recomendado) ou pip
- **Git**: Para clonar o repositório

---

## Instalação

### 1. Instalar uv (Gerenciador de Pacotes)

```bash
# Windows (PowerShell)
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### 2. Configurar Ambiente Virtual

```bash
.venv\Scripts\activate
```

### 3. Instalar Dependências

```bash
uv pip install -r requirements.txt
```

---

## Como Executar

### Passo 1: Preparar Vídeo de Entrada

Coloque seu vídeo MP4 no diretório `data/`:

```bash
data/
└── video.mp4
```

### Passo 2: Executar o Sistema

#### Execução Básica (Configuração Padrão)

```bash
python -m src.main
```

Esta execução:
- Processa o vídeo em `data/video.mp4`
- Gera saídas em `data/outputs/`
- Cria vídeo anotado e relatório completo

#### Execução com Diretório de Entrada Customizado

```bash
python -m src.main --input caminho/para/seu/video.mp4
```

#### Especificar Diretório de Saída

```bash
python -m src.main --output data/resultados/
```

#### Executar Sem Gerar Vídeo de Saída (Apenas Relatório)

```bash
python -m src.main --no-output-video
```
---
