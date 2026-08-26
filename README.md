# 👤 Synthetic People & Avatars Dataset

Um dataset aberto e independente de perfis demográficos e fotos de perfil de alta qualidade em resolução **512x512 JPEG (qualidade 80%)**, projetado para uso seguro e realista em ambientes de desenvolvimento, testes de interface, seeds de banco de dados e demonstrações comerciais.

---

## 🤖 Declaração de Inteligência Artificial e Privacidade

> [!IMPORTANT]
> **Todas as imagens, nomes e dados contidos neste repositório foram gerados 100% por Inteligência Artificial (IA)**.
> 
> - **Nenhum dos rostos ou identidades retrata uma pessoa real existente no mundo real**.
> - Este dataset é livre de dados pessoais sensíveis (LGPD / GDPR compliant por concepção), sendo seguro para exibição em público, gravações de tela, vídeos de demonstração e testes automatizados.

---

## 📐 Especificação Técnica dos Avatares

- **Formato**: JPEG (`.jpg`)
- **Resolução**: `512x512` pixels (proporção 1:1)
- **Qualidade de Compressão**: 80% (otimizada para rápida transferência web/mobile sem perda perceptível de nitidez)
- **Estilo Fotográfico**: Retratos com iluminação suave, enquadramento frontal/três quartos e fundo neutro desfocado.

---

## 🔒 Regras Mandatórias de Manutenção e IDs

Para garantir compatibilidade contínua com aplicações que consomem este dataset como dependência:

1. **Imutabilidade de IDs**:
   - O campo `id` atribuído a cada perfil é **estritamente permanente e NUNCA deve ser modificado, reutilizado ou reordenado**.
2. **Novas Adições**:
   - Ao adicionar novos avatares e perfis ao catálogo, o `id` deve ser sempre **único e estritamente incremental** (`21`, `22`, `23`, ...).
3. **Estrutura de Pastas**:
   - Imagens de adultos devem ser salvas exclusivamente no diretório `adult/`.
   - Imagens de crianças/adolescentes devem ser salvas exclusivamente no diretório `child/`.

---

## 📂 Estrutura do Repositório

```
.
├── README.md       # Documentação e regras do dataset
├── people.json     # Catálogo estruturado de todos os perfis
├── adult/          # Fotos de perfil de adultos (512x512 .jpg)
│   ├── renata.jpg
│   ├── rodrigo.jpg
│   └── ...
└── child/          # Fotos de perfil de crianças (512x512 .jpg)
    ├── enzo.jpg
    ├── helena.jpg
    └── ...
```

---

## 📄 Schema do `people.json`

Cada item da lista `profiles` segue a seguinte estrutura JSON:

| Campo | Tipo | Descrição | Exemplo |
| :--- | :---: | :--- | :--- |
| `id` | `Integer` | Identificador único e imutável | `1` |
| `name` | `String` | Nome completo | `"Renata Silva"` |
| `first_name` | `String` | Primeiro nome | `"Renata"` |
| `last_name` | `String` | Sobrenome | `"Silva"` |
| `category` | `String` | Categoria de faixa etária (`"adult"` ou `"child"`) | `"adult"` |
| `gender` | `String` | Gênero (`"female"` ou `"male"`) | `"female"` |
| `age` | `Integer` | Idade em anos | `32` |
| `avatar_file` | `String` | Caminho relativo do arquivo de imagem | `"adult/renata.jpg"` |

---

## 📦 Exemplo de Consumo

```json
{
  "id": 1,
  "name": "Renata Silva",
  "first_name": "Renata",
  "last_name": "Silva",
  "category": "adult",
  "gender": "female",
  "age": 32,
  "avatar_file": "adult/renata.jpg"
}
```
