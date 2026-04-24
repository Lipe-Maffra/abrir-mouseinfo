# Abrir MouseInfo

Projeto simples em Python para abrir a ferramenta `mouseInfo()` da biblioteca `MouseInfo`.

O objetivo e facilitar a captura de coordenadas do mouse para uso em automacoes de interface, testes ou scripts com bibliotecas como `PyAutoGUI`.

## O que este projeto faz

- executa `mouseInfo()` a partir do arquivo `main.py`
- oferece um atalho via `abrir_mouseinfo.bat` para uso no Windows
- mantem as dependencias registradas em `requirements.txt`

## Estrutura do projeto

```text
abrir_mouseinfo/
|-- abrir_mouseinfo.bat
|-- main.py
|-- requirements.txt
|-- .gitignore
`-- README.md
```

## Requisitos

- Windows
- Python 3.11 ou superior
- `venv` habilitado na instalacao do Python

Versao usada no desenvolvimento: `Python 3.11.9`

Para verificar sua versao instalada:

```powershell
python --version
```

## Instalacao

Crie o ambiente virtual:

```powershell
python -m venv .venv
```

Ative o ambiente:

```powershell
.venv\Scripts\activate
```

Instale as dependencias:

```powershell
pip install -r requirements.txt
```

## Como executar

### Opcao 1: executar pelo Python

Com o ambiente virtual ativado:

```powershell
python main.py
```

### Opcao 2: executar pelo arquivo `.bat`

O arquivo `abrir_mouseinfo.bat` foi pensado para uso no Windows. Antes de rodar, ajuste esta linha:

```bat
cd /d "Caminho do seu codigo"
```

Substitua pelo caminho real da pasta do projeto. Exemplo:

```bat
cd /d "C:\Users\felipe.maffra\Desktop\Python\abrir_mouseinfo"
```

Depois disso, basta executar:

```powershell
.\abrir_mouseinfo.bat
```

## Arquivos principais

### `main.py`

Arquivo responsavel por abrir a interface do MouseInfo:

```python
from mouseinfo import mouseInfo

mouseInfo()
```

### `requirements.txt`

Dependencias atuais do projeto:

```text
MouseInfo==0.1.3
pyperclip==1.11.0
```

## Problemas comuns

### Erro: `No module named 'mouseinfo'`

Ative o ambiente virtual e reinstale as dependencias:

```powershell
.venv\Scripts\activate
pip install -r requirements.txt
```

### Erro: caminho nao encontrado no `.bat`

Revise o valor usado no comando `cd /d` dentro de `abrir_mouseinfo.bat`. O caminho precisa apontar exatamente para a pasta onde esta o arquivo `main.py`.

## Observacoes

- A pasta `.venv` nao faz parte do repositorio e deve ser criada localmente.
- O projeto foi pensado para uso em ambiente Windows.
- O arquivo `.bat` depende de um caminho valido no seu computador.

## Autor

Felipe Vieira Maffra
