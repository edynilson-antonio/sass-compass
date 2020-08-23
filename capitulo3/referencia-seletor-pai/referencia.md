# Referência ao seletor-pai &

Usar o & para fazer referência, nessa sintaxe podemos definir seletores separados por hífen (-) ou underscore (_).

Exemplo Sass:
```
.lateral {
    color: red;

    &-menu {
        color: blue;
    }

    &_social {
        color: orange;
    }
}
```

Saída:
```
.lateral {
    color: red;
}

.lateral-menu {
    color: blue;
}

.lateral_social {
    color: orange;
}
```