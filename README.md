# 🌳 Arco do Desmatamento — Cartografia da Perda Florestal na Amazônia Legal

> Mapa de geoprocessamento produzido no QGIS, representando o avanço anual do desmatamento na Amazônia Legal com base nos dados oficiais do PRODES/INPE.

---

## 📍 Objetivo

Este mapa tem como objetivo visualizar espacialmente o **incremento anual de desmatamento** na Amazônia Legal entre 2008 e os anos mais recentes disponíveis, destacando a região conhecida popularmente como **"Arco do Desmatamento"** — uma faixa de pressão antrópica que avança sobre a floresta a partir de seus limites sul e leste. O produto foi desenvolvido como parte da formação em geoprocessamento e análise espacial, servindo como peça de portfólio técnico-científico.

---

## 🗺️ Visualização do Mapa

![Mapa do Arco do Desmatamento — Amazônia Legal](outputs/Mapa%20do%20Arco%20do%20Desmatamento%20com%20Autoria.png)

> **Arquivo completo em alta resolução:** [`Mapa do Arco do Desmatamento Com Autoria.pdf`](outputs/Mapa%20do%20Arco%20do%20Desmatamento%20Com%20Autoria.pdf)

> ⚠️ **Nota:** o PDF tem ~740 MB e **não pode ser enviado ao GitHub** (limite de 100 MB). Suba apenas o PNG. O PDF fica salvo localmente ou em serviço externo (Google Drive, etc.).

---

## 📦 Fonte de Dados

| Item | Detalhes |
|---|---|
| **Dataset** | Incremento Anual de Desmatamento — PRODES |
| **Produtor** | Instituto Nacional de Pesquisas Espaciais (INPE) |
| **Plataforma de acesso** | [TerraBrasilis](http://terrabrasilis.dpi.inpe.br/) |
| **Cobertura temporal** | 2008 até o ano mais recente disponível |
| **Cobertura espacial** | Amazônia Legal, Brasil |
| **Licença dos dados** | [Creative Commons Atribuição-CompartilhaIgual 4.0 Internacional (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.pt_BR) |
| **Projeção** | SIRGAS 2000 / Geográficas (EPSG:4674) |

> ℹ️ **Nota sobre dados brutos:** os shapefiles originais do PRODES não estão incluídos neste repositório. Os dados de origem são públicos e disponíveis em [TerraBrasilis/INPE](http://terrabrasilis.dpi.inpe.br/). A cartografia, a simbologia e o layout são de autoria própria.

---

## 🔬 Metodologia

### 1. Obtenção dos Dados
- Download da camada de **incremento anual de desmatamento** (formato shapefile) via plataforma TerraBrasilis/PRODES.

### 2. Processamento no QGIS
- Importação e inspeção dos atributos da camada vetorial.
- **Filtragem** dos polígonos de incremento por ano de detecção, mantendo o período de análise desejado.
- **Simbologia categorizada por ano:** cada ano recebe uma cor distinta em gradiente cromático, do mais antigo (cores mais frias) ao mais recente (cores mais quentes), evidenciando a progressão temporal do desmatamento.
- Definição do **Sistema de Referência de Coordenadas:** SIRGAS 2000 (EPSG:4674), padrão geodésico oficial do Brasil.

### 3. Montagem do Layout Cartográfico
O layout final foi composto no **Gerenciador de Layouts** do QGIS, contendo:
- 🗺️ Mapa principal com a camada de desmatamento e limite da Amazônia Legal
- 📋 **Legenda** com categorias por ano
- 📏 **Escala gráfica**
- 🧭 **Seta Norte**
- 🔲 **Grade de coordenadas geográficas**
- Fontes e créditos institucionais

### 4. Exportação
- Exportado em formato **PDF** (alta resolução) e **PNG** para uso web.

---

## 🛠️ Ferramentas Utilizadas

| Ferramenta | Finalidade |
|---|---|
| [QGIS](https://qgis.org/) (versão 3.x) | Processamento, simbologia e composição cartográfica |
| TerraBrasilis (INPE) | Plataforma de acesso aos dados de origem (PRODES) |

---

## 📁 Estrutura do Repositório

```
📦 arco-desmatamento/
├── 📄 README.md                                        ← Este arquivo
├── 📄 .gitignore                                       ← Arquivos ignorados pelo Git
├── 📄 LICENSE                                          ← Licença de uso
│
├── 📂 outputs/                                         ← Produtos cartográficos finais (autorais)
│   ├── Mapa do Arco do Desmatamento Com Autoria.pdf    ← PDF (salvo localmente, ~740 MB)
│   └── Mapa do Arco do Desmatamento com Autoria.png   ← PNG para visualização web
│
├── 📂 data/
│   ├── 📂 raw/                ← Dados brutos (NÃO versionados — ver .gitignore)
│   │   └── .gitkeep
│   └── 📂 processed/          ← Dados processados leves (ex.: GeoJSON filtrado)
│       └── .gitkeep
│
└── 📂 docs/                   ← Documentação complementar (opcional)
    └── metodologia.md
```

---

## 👤 Sobre o Autor

**Augusto Murça**
Estudante de **Sistemas de Informação** (3º semestre) na Universidade Federal Rural da Amazônia (UFRA).
Pesquisador de iniciação científica **PIBIC** na interface entre **epidemiologia espacial** e geotecnologias, com vínculo ao **INPE/Fiocruz**.
Trabalha com geoprocessamento, análise espacial e dados ambientais utilizando **QGIS, Python e R**.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Conectar-0A66C2?style=flat&logo=linkedin)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-Perfil-181717?style=flat&logo=github)](https://github.com)

---

## 📜 Licença

Este repositório — incluindo o mapa, layout cartográfico, simbologia e documentação — está licenciado sob **Creative Commons Atribuição-NãoComercial-SemDerivações 4.0 Internacional (CC BY-NC-ND 4.0)**.

[![CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.pt_BR)

**Você pode:** compartilhar o material com atribuição ao autor.
**Você não pode:** usar comercialmente, modificar, adaptar ou criar obras derivadas.

© 2025 Augusto Murça. Todos os direitos reservados sobre a obra cartográfica.

Os **dados de origem** (PRODES/INPE) são públicos e seguem a licença **CC BY-SA 4.0** do produtor.

---

*Mapa produzido como parte da formação em geoprocessamento e análise espacial. Dados oficiais do PRODES/INPE.*
