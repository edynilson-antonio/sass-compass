# Escopo de Variáveis

- Escopo global
- Escopo local



**Exemplo:**
```
$cor_um: lime;
$cor_dois: black;

p {
    $cor_um: red; // válido somente para esta regra CSS
    color: $cor_um;
    background: $cor_dois;
}

div {
  color: $cor_um;
  background: $cor_dois;
}
```

**Saída:**

```
p {
  color: red;
  background: black;
}

div {
  color: lime;
  background: black;
}
```

### Flag !global

É possível fazer com que uma variável definida em escopo local seja redefinida para o global com uso dessa flag.

**Exemplo:**

```
$cor_um: lime;
$cor_dois: black;

p {
    $cor_um: red !global; // vai para o escopo global
    color: $cor_um;
    background: $cor_dois;
}

div {
  color: $cor_um;
  background: $cor_dois;
}
```

### Flag !default

Permite a definação de uma variável em escopo local seja válida, somente no caso em que ela não tenha sido definida no escopo global.

**Exemplo:**

```
$cor_um: lime;
$cor_dois: black;

p {
    $cor_um: red !default; // não será válida
    color: $cor_um;
    background: $cor_dois;
}

div {
  color: $cor_um;
  background: $cor_dois;
}
```