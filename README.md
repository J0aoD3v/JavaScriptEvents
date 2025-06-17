# Seminário Prático de Eventos em JavaScript

Este projeto é uma prática didática sobre os **eventos mais comuns em JavaScript**, com foco no uso de eventos diretamente em elementos HTML, como `onclick`, `onmouseover`, `onmouseout`, `onkeydown`, `onchange`, entre outros.

O exercício foi proposto para aplicar conceitos fundamentais de manipulação de DOM e eventos.

## 🔧 Estrutura do Projeto

O projeto possui um único arquivo principal:

- `index.html`: arquivo HTML contendo todos os elementos e scripts para os eventos JS.

## 💡 Eventos Demonstrados

O código base ilustra o uso dos seguintes eventos:

| Evento        | Ação                                                             |
|---------------|------------------------------------------------------------------|
| `onload`      | Exibe mensagem ao carregar a página.                             |
| `onclick`     | Ação ao clicar no botão.                                          |
| `onmouseover` | Muda a cor da `div.box` ao passar o mouse.                        |
| `onmouseout`  | Restaura a cor original da `div.box` ao remover o mouse.          |
| `onkeydown`   | Detecta tecla pressionada no campo de texto.                      |

---

## 📚 Desafios Propostos e Soluções

### ✅ Desafio 1: Modificando o `onclick`

**Objetivo:** Alterar a função `exibirAlerta()` para que, em vez de mostrar um alert, mude o texto do `<h1>` para `"Botão Clicado!"`.

**Solução:**
```javascript
function exibirAlerta() {
    document.querySelector('h1').textContent = 'Botão Clicado!';
    infoParagraph.textContent = 'Evento "onclick" disparado e H1 alterado.';
}
```

---

### ✅ Desafio 2: Usando `onchange`

**Objetivo:** Adicionar um novo campo de input. Quando o usuário digitar algo e sair do campo, o texto digitado deve aparecer dentro da `div.box`.

**HTML Adicional:**

```html
<input type="text" onchange="atualizarBox(this)" placeholder="Digite algo e clique fora...">
```

**Função JavaScript:**

```javascript
function atualizarBox(inputElemento) {
    const box = document.querySelector('.box');
    box.textContent = inputElemento.value;
    infoParagraph.textContent = 'Evento "onchange" disparado!';
}
```

---

### ✅ Desafio 3: Combinando Eventos com `ondblclick`

**Objetivo:** Fazer com que um duplo clique na `div.box` mude a cor da borda para vermelho.

**HTML Modificado:**

```html
<div class="box"
     onmouseover="mudarCorFundo(this, 'lightblue')"
     onmouseout="mudarCorFundo(this, 'lightgray')"
     ondblclick="mudarBorda(this)">
    Passe o mouse sobre mim
</div>
```

**Função JavaScript:**

```javascript
function mudarBorda(elemento) {
    elemento.style.borderColor = 'red';
    infoParagraph.textContent = 'Evento "ondblclick" disparado!';
}
```

---

## 📂 Arquivo Original (`index.html`)

Você pode ver o conteúdo original e modificado acessando o [repositório completo no GitHub](https://github.com/J0aoD3v/JavaScriptEvents).

---

## 🧠 Aprendizados

Este exercício prático permitiu explorar os seguintes conceitos:

* Interação com elementos HTML via JavaScript.
* Manipulação de propriedades do DOM (como `textContent`, `style`, etc).
* Uso de eventos para tornar a interface mais dinâmica.
* Implementação de eventos combinados e múltiplos comportamentos em uma só página.

---

## 🚀 Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/J0aoD3v/JavaScriptEvents
   ```
2. Abra o arquivo `index.html` no navegador.
3. Interaja com os elementos e observe os eventos sendo disparados.

---

## 👨‍💻 Autor

**João Cláudio F. M. C.**
📘 Acadêmico de Ciência da Computação - UENP
🔗 GitHub: [@J0aoD3v](https://github.com/J0aoD3v)

---

## 📝 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
```
