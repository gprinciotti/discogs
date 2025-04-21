# Discogs

Análise exploratória sobre tendências na música brasileira utilizando a base de dados do [Discogs](https://www.discogs.com/). Os dados foram extraídos dos *dumps* mais recentes e processados localmente. Para detalhes sobre a estrutura da base, consulte a [documentação da API do Discogs](https://www.discogs.com/developers).

## Sumário

- [Sobre o Projeto](#sobre-o-projeto)
- [Fluxo de Dados](#fluxo-de-dados)
- [Configuração do Ambiente](#configuração-do-ambiente)
- [Autor](#autor)
- [Licença](#licença)

## Sobre o Projeto

Este projeto tem como objetivo explorar a evolução dos estilos musicais e as relações entre artistas brasileiros ao longo do tempo, com base nos metadados disponibilizados pelo Discogs. A análise inclui gráficos descritivos da produção musical em diferentes estilos e períodos, utilizando Python e DuckDB para manipulação de dados.

## Fluxo de Dados

1. **Download dos *dumps* do Discogs**: a versão mais recente dos dados (abril de 2025) foi baixada manualmente da página https://discogs-data-dumps.s3.us-west-2.amazonaws.com/index.html.

2. **Conversão de XML para CSV**: a ferramenta [discogs-xml2db](https://github.com/philipmat/discogs-xml2db) foi utilizada para extrair os dados relevantes (e.g. *artists*, *releases*, etc.) e convertê-los em arquivos .csv.

3. **Criação de banco DuckDB**: todos os arquivos .csv foram importados e organizados em um banco de dados local utilizando [DuckDB](https://duckdb.org/).

## Configuração do Ambiente

Para configurar seu ambiente para executar este projeto, siga as instruções abaixo:

1. **Pré-requisitos**: Certifique-se de ter Python 3.13+ instalado.

2. **Poetry**: Este projeto utiliza o [Poetry](https://python-poetry.org/) para gerenciar o ambiente virtual e as dependências. Certifique-se de que o Poetry está instalado.

```bash
# Criar e ativar o ambiente com Poetry
poetry install

# Para iniciar o ambiente virtual
poetry env activate
```

## Autor

Desenvolvido por **Vinicius Princiotti**.
- Email: [vinicius.princiotti@gmail.com](mailto:vinicius.princiotti@gmail.com)

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).