Excelente observação 👌 — o fenômeno que você está descrevendo chama-se, em tipografia, um **“órfão tipográfico”** (ou, mais precisamente, **“viúva” ou “órfã de linha”** — no inglês, _widow/orphan control_).

Mas no caso **específico do LaTeX**, o que você quer evitar são **“viúvas de uma única letra”**, ou seja, **preposições e artigos isolados no final de linha** (_a_, _o_, _de_, _em_, _à_ etc.).
O nome técnico do recurso que previne isso é o uso de **espaço inquebrável**, em inglês: **non-breaking space**.

---

## 💡 Nome do recurso

> 🔸 **Espaço inquebrável** (_non-breaking space_)

---

## 🧩 Como usar no LaTeX

Use a **til (~)** entre as palavras que não devem se separar:

```latex
consequentemente~à
período~de~11~a~24~de~maio~de~2025
```

Assim o LaTeX trata o `~` como um **espaço normal**, mas **impede a quebra de linha** naquele ponto.

---

## 🧠 Explicação técnica

- `~` é o **espaço inquebrável** (_non-breaking space_) em LaTeX.
- Ele é equivalente a `&nbsp;` no HTML.
- Mantém o espaçamento normal, mas nunca permite quebra ali.
- Exemplo visual:

  ```
  período~de~11~a~24
  ```

  fica sempre junto, mesmo se o texto for justificado.

---

## 🧱 Recurso automático de Expressão regular

Não existe um comando nativo que insira automaticamente esses `~`,
mas alguns editores (como o Overleaf, TeXstudio, VS Code + macros) permitem automatizar via regex.

Por exemplo, uma expressão regular para localizar preposições soltas (em português):

### Solução no VSCODE

(\s+|~)([aAoOsSeéÉEàÀ],?)\s+
$1$2~

### Solução Genérica

```
(\s)([aAoOsSeéÉEàÀ])\s
```

…e substituir por:

```
\1\2~
```

Isso coloca automaticamente o `~` após artigos e preposições curtas.

---

✅ **Resumo**

| Situação                               | Nome do recurso                           | Símbolo no LaTeX | Exemplo              |
| -------------------------------------- | ----------------------------------------- | ---------------- | -------------------- |
| Evitar letras sozinhas no fim da linha | Espaço inquebrável (_non-breaking space_) | `~`              | `consequentemente~à` |

---

Se quiser, posso te mostrar um **script (regex)** para aplicar automaticamente esses `~` em todo o texto `.tex` — ideal para revistas ou livros. Deseja isso?

