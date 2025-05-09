# 📚 Extrator de Dados Estruturados de TCCs usando OpenAI

Este projeto realiza a extração automática de informações de Trabalhos de Conclusão de Curso (TCCs) em arquivos `.pdf` e `.docx`, utilizando modelos da OpenAI. As informações extraídas são organizadas em arquivos `.json`, prontos para análise ou armazenamento.

---

## 🚀 Funcionalidades

- Leitura de arquivos `.pdf` e `.docx`
- Extração de trechos textuais importantes (Resumo, Introdução, Conclusão, etc.)
- Conversão das informações extraídas para formato JSON estruturado
- Armazenamento dos resultados em uma pasta específica
- Utilização de API da OpenAI com modelo `gpt-4o-mini` para interpretação e organização dos dados

---

## 🛠️ Tecnologias utilizadas

- [Python 3.x](https://www.python.org/)
- [OpenAI API](https://platform.openai.com/)
- [python-dotenv](https://pypi.org/project/python-dotenv/)
- [PyPDF2](https://pypi.org/project/PyPDF2/)
- [python-docx](https://python-docx.readthedocs.io/en/latest/)

---

## 📂 Estrutura de Pastas

📁 projeto tcc/ <br>
├── 📁 resultados_json <br>
├── 📁 TCCs <br>
├── 📁 venv <br>
├── .env <br>
└── extracao-varios-tccs.ipnyb <br>

## 🔧 Configuração

1. **Clone o projeto**:

```bash
git clone https://github.com/Iuis-felipe/extracao-de-dados-utilizando-ia.git
```

2. **Crie um ambiente virtual:**:

```bash
python -m venv venv

# Ativar no Windows
venv\Scripts\activate

# Ativar no Linux/Mac
source venv/bin/activate
```

3. **Instale as dependências**:

```bash
pip install -r requirements.txt
```

4. **Configure a variável de ambiente:**:

Crie um arquivo .env na raiz do projeto com o seguinte conteúdo:

```bash
OPENAI_API_KEY=sua-chave-aqui
```

5. **Organize os arquivos:**:

- Coloque os arquivos .pdf ou .docx dos TCCs em uma pasta chamada TCCs.

- O script irá salvar os arquivos .json extraídos em uma pasta chamada resultados_json.

5. **Execute o script:**:

Por fim, basta executar o script no compilador.

---

## 📋 Exemplo de JSON Gerado

```Bash
{
    "Autor": "Nome do Autor",
    "Título": "Título do TCC",
    "Ano de publicação": "2024",
    "Local de publicação": "Nome da Instituição",
    "Orientador(a)": "Nome do Orientador",
    "Coorientador(a)": "Nome do Coorientador",
    "Resumo": "Texto completo do resumo...",
    "Palavras-chave": ["palavra1", "palavra2", "palavra3"],
    "Introdução": "Texto completo da introdução...",
    "Conclusão": "Texto completo da conclusão..."
}
```