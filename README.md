# FNAF API 

API RESTful com informações sobre os personagens (animatronics) da franquia **Five Nights at Freddy's (FNAF)**, incluindo dados como nome, jogo de origem, altura, resumo da lore e estratégias de defesa.

## 📖 Sobre o projeto

Esta API foi criada para fornecer, de forma simples e estruturada, dados sobre os animatronics de todos os jogos da série FNAF. Ideal para uso em projetos front-end, aplicativos, sites de fãs, quizzes ou qualquer aplicação que precise consumir informações sobre o universo do jogo.

## 🗂️ Estrutura dos dados

Cada personagem retornado pela API segue o seguinte formato:

```json
{
  "id": 35,
  "name": "Ennard",
  "game": "FNAF Sister Location",
  "height": "2.4m",
  "summary": "Ennard é uma criatura formada pela fusão de vários animatronics da instalação. Uma massa de fios, máscaras e peças metálicas que se unem em uma única entidade. Seu verdadeiro objetivo é escapar da instalação usando o corpo de um humano como disfarce. Entre todos os inimigos da série, Ennard representa talvez a maior prova de que algo muito mais sombrio está acontecendo por trás das cortinas da Fazbear Entertainment.",
  "defense": "Evite cometer erros durante os eventos finais da história.",
  "image": "Ennard-removebg-preview.png"
}
```

### Campos

| Campo     | Tipo   | Descrição                                                   |
|-----------|--------|--------------------------------------------------------------|
| `id`      | number | Identificador único do personagem                            |
| `name`    | string | Nome do animatronic                                          |
| `game`    | string | Jogo da franquia em que o personagem aparece                 |
| `height`  | string | Altura aproximada do personagem                              |
| `summary` | string | Resumo/lore sobre o personagem                                |
| `defense` | string | Estratégia ou dica para se defender/sobreviver ao personagem  |
| `image`   | string | Nome do arquivo de imagem associado ao personagem             |

## 🚀 Como usar

Este projeto **não possui um servidor/backend** — os dados ficam em arquivo(s) `.json` dentro do próprio repositório, junto com as imagens dos personagens. Para consumir os dados, basta acessar o conteúdo bruto (raw) do GitHub.

### 1. Clonando o repositório

```bash
git clone https://github.com/seu-usuario/fnaf-api.git
```

Depois é só importar o arquivo JSON diretamente no seu projeto (Node, front-end, etc).

### 2. Consumindo direto pela internet (sem clonar)

Você pode buscar os dados usando a URL "raw" do GitHub, no formato:

```
https://raw.githubusercontent.com/seu-usuario/fnaf-api/main/CAMINHO/DO/ARQUIVO.json
```

**Exemplo com fetch (JavaScript):**
```js
fetch("https://raw.githubusercontent.com/seu-usuario/fnaf-api/main/characters.json")
  .then(response => response.json())
  .then(data => console.log(data));
```

**Exemplo com Python:**
```python
import requests

url = "https://raw.githubusercontent.com/seu-usuario/fnaf-api/main/characters.json"
data = requests.get(url).json()
print(data)
```

## 🖼️ Imagens

As imagens dos personagens ficam armazenadas no repositório e são referenciadas pelo campo `image` de cada personagem. Para exibi-las, monte a URL raw apontando para a pasta onde elas estão:

```
https://raw.githubusercontent.com/seu-usuario/fnaf-api/main/images/Ennard-removebg-preview.png
```

> ⚠️ Recomenda-se organizar as imagens em uma pasta própria (ex: `/images`) e manter os arquivos JSON separados por jogo ou em um único arquivo (ex: `characters.json`), facilitando a navegação e o consumo dos dados.

## 🛠️ Tecnologias utilizadas

- JSON (armazenamento dos dados)
- GitHub (hospedagem dos arquivos e imagens)

> Se no futuro você adicionar um servidor (Node/Express, json-server, etc.), essa seção e a de uso devem ser atualizadas com os endpoints reais.

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests com novos personagens, correções ou melhorias na API.

## 📄 Licença

Este projeto é distribuído sob a licença MIT. FNAF e seus personagens são propriedade da Scott Cawthon / Steel Wool Studios — este projeto é apenas um trabalho de fã, sem fins comerciais.
