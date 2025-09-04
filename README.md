# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas linguagens Python, JavaScript, TypeScript e Java, e gera relatórios `HTML` como [este](https://andrehora.github.io/gitevo-examples/python/pandas.html).

Mais exemplos de relatórios podem ser podem ser encontrados em https://github.com/andrehora/gitevo-examples.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

> [!NOTE]
> Antes de instalar a ferramenta, é recomendado criar e ativar um [ambiente virtual Python](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#create-and-use-virtual-environments).

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
$ pip install gitevo
```

Execute a ferramenta no repositório selecionado utilizando o comando abaixo (ajuste conforme a linguagem do repositório).
Substitua `<git_url>` pela URL do repositório que será analisado:

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r js <git_url>

# TypeScript
$ gitevo -r ts <git_url>

# Java
$ gitevo -r java <git_url>
```

Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

> [!NOTE]
> Essa etapa pode demorar alguns minutos pois o projeto será clonado e analisado localmente.

# Passo 3: Explorar o relatório de evolução de código

Após executar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), é gerado um relatório `HTML` contendo diversos gráficos sobre a evolução do código.

Abra o relatório `HTML` e observe com atenção os gráficos.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo
- Detalhar se as curvas estão de acordo com boas práticas
- Explicar grandes alterações nas curvas
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- etc.

Seja criativo!

# Instruções para o exercício

1. Crie um `fork` deste repositório (mais informações sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Adicione o relatório `HTML` no seu fork.
3. No Moodle, submeta apenas a URL do seu `fork`.

Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork:

1. Repositório selecionado: python https://github.com/huggingface/transformers.git
2. Gráfico selecionado: 
 ![Lines of code](loc_evolution.png)
3. Explicação: 
## ANÁLISE DA EVOLUÇÃO DO CÓDIGO: Hugging Face Transformers

### Introdução

O gráfico selecionado apresenta a evolução das linhas de código (LOC) do repositório Hugging Face Transformers ao longo do período de 2020 a 2025. Esta análise permite compreender o crescimento exponencial de um dos projetos open source mais significativos na área de inteligência artificial.

### Dados Analisados

O gráfico revela os seguintes valores de linhas de código:
- **2020:** 70.083 LOC
- **2021:** 258.442 LOC (+269% de crescimento)
- **2022:** 581.466 LOC (+125% de crescimento)
- **2023:** 961.102 LOC (+65% de crescimento)
- **2024:** 1.273.945 LOC (+33% de crescimento)
- **2025:** 1.540.371 LOC (+21% de crescimento)

### Análise dos Resultados

#### Fase de Crescimento Exponencial (2020-2021)

O período de 2020-2021 apresenta o maior crescimento percentual (269%), caracterizando uma fase de expansão acelerada. Este crescimento coincide com fatores externos significativos:

- **Contexto tecnológico:** Lançamento do GPT-3 pela OpenAI em 2020
- **Adoção empresarial:** Integração massiva de modelos de linguagem em produtos comerciais
- **Evolução da biblioteca:** Implementação de pipelines e integração com Hugging Face Hub

#### Fase de Consolidação (2021-2025)

A partir de 2021, observa-se uma desaceleração gradual do crescimento:
- **2021-2022:** +125% (crescimento ainda elevado)
- **2022-2023:** +65% (desaceleração natural)
- **2023-2024:** +33% (crescimento maduro)
- **2024-2025:** +21% (estabilização)

### Correlação com Arquivos Python

A análise correlacionada com o número de arquivos Python revela:
- **2020:** 202 arquivos Python
- **2025:** 3.365 arquivos Python

O crescimento proporcional (16,7x) indica uma arquitetura modular bem estruturada.

### Métricas de Qualidade

#### LOC por Arquivo Python
- **2020:** 346,9 LOC/arquivo
- **2025:** 457,8 LOC/arquivo

O aumento de 32% no tamanho médio dos arquivos sugere maior complexidade dos modelos implementados.

### Principais Alterações Identificadas

#### 2021: Expansão Arquitetural
- Implementação de suporte a múltiplos frameworks (PyTorch, TensorFlow, JAX)
- Adição de dezenas de novos modelos
- Desenvolvimento de pipelines de processamento

#### 2023: Era Multimodal
- Integração de modelos de visão (ViT, CLIP, DETR)
- Implementação de modelos de áudio (Wav2Vec2, Whisper)
- Desenvolvimento de modelos multimodais

### Conclusões

O gráfico demonstra a evolução de um projeto acadêmico para uma infraestrutura crítica da indústria de IA. O crescimento de 22x em 5 anos, mantendo qualidade e usabilidade, representa um caso de sucesso raro no desenvolvimento de software open source.

### Limitações e Considerações

- **Complexidade crescente:** 1,5M+ linhas podem impactar manutenibilidade
- **Curva de aprendizado:** Pode dificultar contribuições de novos desenvolvedores
- **Performance:** Código extenso pode afetar tempo de build e testes

### Referências

- Dados obtidos através da ferramenta GitEvo
- Repositório: huggingface/transformers
- Período de análise: 2020-2025