# deja-vu-2

📌 Continuação do experimento iniciado em [deja-vu](https://github.com/D166er/deja-vu).  
Um utilitário de terminal simples para salvar e reutilizar comandos com **aliases nomeados**.

---

## ✨ Novidades em relação ao deja-vu original
- Suporte a **aliases compostos aninhados** (um combinado pode usar outro combinado).
- Listagem (`-l`) mais limpa → mostra apenas o primeiro item + `...` quando há muitos.
- Remoção com dependência:
  - `-r NOME` → remove apenas se não houver dependentes.
  - `-r -f NOME` → remove `NOME` e **todos os dependentes em cascata**.

---

## 🔧 Instalação
1. Baixe o repositório e coloque o `deja-vu.py` no seu `PATH`, por exemplo:
   ```bash
   chmod +x deja-vu.py
   cp deja-vu.py ~/.local/bin/deja-vu
   ```
2. Certifique-se de que `~/.local/bin` está no `PATH`.

---

## 🚀 Uso

### Adicionar comando simples
```bash
deja-vu -a ampliar pdf -- pdfposter -s2 input.pdf output.pdf
```

### Adicionar comando combinado
```bash
deja-vu -a fazer poster -c conv. img pdf, ampliar pdf
```

### Mostrar comandos
```bash
deja-vu -s fazer poster
```

### Listar todos
```bash
deja-vu -l
```

### Remover
```bash
deja-vu -r ampliar pdf      # erro se houver dependentes
deja-vu -r -f ampliar pdf   # remove ampliado e dependentes
```

---

## 📖 Histórico do experimento
- O primeiro projeto (**deja-vu**) mostrou que até um leigo em programação consegue, com linguagem natural, construir uma ferramenta real e útil junto com IA.
- Este repositório (**deja-vu-2**) continua o experimento, adicionando funções de **validação, limpeza e remoção em cascata**.
- O código segue simples e legível, contrariando a ideia de que IA gera programas “imanuteníveis”.
