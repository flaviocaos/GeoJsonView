# GeoJSON View v2.0

Aplicação web interativa para visualização, edição e análise de dados geoespaciais em formato GeoJSON, com integração de camadas temáticas WMS do IBGE.

![GeoJSON View](https://img.shields.io/badge/versão-2.0-blue) ![Licença](https://img.shields.io/badge/licença-MIT-green) ![HTML](https://img.shields.io/badge/linguagem-HTML%2FCSS%2FJS-orange)

---

## Descrição

O GeoJSON View é uma ferramenta leve e de arquivo único (`index.html`) voltada para profissionais e entusiastas de geotecnologias. Permite carregar, visualizar, editar e exportar dados espaciais diretamente no navegador, sem necessidade de instalação ou servidor.

---

## Funcionalidades

### Visualização
- Carregamento de arquivos GeoJSON por clique ou **arrastar e soltar (drag & drop)**
- Suporte a geometrias do tipo Ponto, Linha e Polígono
- Ajuste automático do mapa ao extent da camada carregada
- Exibição de coordenadas em tempo real ao mover o cursor

### Edição
- Ferramentas de desenho: polígono, linha, retângulo e marcador (via Leaflet-Draw)
- Seleção de cor do traço com paleta de 5 cores
- Controle de opacidade de preenchimento via slider
- Destaque visual da feição selecionada

### Camadas
- **4 camadas base:** OpenStreetMap, Satélite ESRI, Topográfico e CartoDB Dark
- **5 camadas temáticas WMS do IBGE:** Meio Ambiente, Agricultura, Recursos Hídricos, Florestas e Índices Econômicos
- Painel de camadas integrado na interface

### Painel Lateral (4 abas)
| Aba | Conteúdo |
|-----|----------|
| **Atributos** | Tabela com propriedades da feição selecionada |
| **Feições** | Lista navegável com busca/filtro e contadores por tipo |
| **Análise** | Área total, comprimento total, bounding box e centróide via Turf.js |
| **Camadas** | Controle de camadas base e WMS |

### Outras Funcionalidades
- **Busca de endereço** via geocodificação (Nominatim/OpenStreetMap)
- **Exportação** do GeoJSON (incluindo feições desenhadas) para arquivo `.geojson`
- **Rótulos** ativáveis/desativáveis nas feições
- Painel lateral recolhível
- Notificações visuais (toast) para todas as ações
- Tema escuro moderno

---

## Tecnologias

| Biblioteca | Versão | Uso |
|------------|--------|-----|
| [Leaflet](https://leafletjs.com/) | 1.9.4 | Renderização e manipulação do mapa |
| [Leaflet-Draw](https://github.com/Leaflet/Leaflet.draw) | 1.0.4 | Ferramentas de desenho e edição |
| [Turf.js](https://turfjs.org/) | 6.5.0 | Análises geoespaciais (área, comprimento, centróide) |
| WMS IBGE | — | Camadas temáticas externas |
| Nominatim | — | Geocodificação de endereços |

> Todas as bibliotecas são carregadas via **cdnjs.cloudflare.com**, sem necessidade de instalação.

---

## Como Usar

1. **Abrir:** Faça o download do `index.html` e abra em qualquer navegador moderno
2. **Carregar dados:** Clique em "Carregar GeoJSON" ou arraste um arquivo `.geojson` para a tela
3. **Explorar:** Clique em uma feição para ver seus atributos no painel lateral
4. **Analisar:** Vá até a aba "Analise" e clique em "Calcular Analises"
5. **Desenhar:** Use a barra de ferramentas do mapa para criar novas feições
6. **Exportar:** Clique em "Exportar" para salvar o GeoJSON atualizado
7. **Buscar:** Digite um endereço na barra superior e pressione Enter

---

## Estrutura do Projeto

```
GeoJsonView/
├── index.html   # Aplicação completa (HTML + CSS + JavaScript)
├── README.md
└── LICENSE
```

---

## Requisitos

- Navegador moderno com suporte a ES5+
- Conexão com a internet (para carregar bibliotecas e camadas WMS)

---

## Licença

Distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
