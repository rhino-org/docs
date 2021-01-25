# Rhino CSS

Framework e Helpers CSS para desenvolvimento.



## Utilizando via CDN

Adicione a seguinte linha antes do fechamento da tad html `</html`>
```html
<link rel="stylesheet" href="http://rhino.org.s3-website-sa-east-1.amazonaws.com/css/rhino-lastest.min.css">
```

Caso queira utilizar alguma versão específica, é só você substituir na URL o `latest` pelo número da versão, por exemplo:

```html
<link rel="stylesheet" href="http://rhino.org.s3-website-sa-east-1.amazonaws.com/css/rhino-1.0.0.min.css">
```

Se por algum motivo deseja acessar o arquivo não-minificado, é só retirar o `.min` da url.

 ---

## Colunas
Você pode controlar a diagramação das colunas do seu layout com muita facilidade, é assim:
- No elemento pai, adicione a classe `cold` e, a partir dai, você terá controle da diagramação de todos os elementos filhos. Veja o exemplo:

```html 
<div class="cols">

    <div class="col-2-3">
        1º Coluna
    <div>
    <div class="col-1-3">
        2º Coluna
    <div>

</div>
````

Dessa forma, você terá 2 colunas, onde a primeira ocupará 2/3 do espaço e a segunda 1/3.
Isso dá muito mais flexibidlidade ao seu desenvolvimento, pois você não precisa mais ficar preso ao conceito das 12 colunas (como é usado no Bootstrap).

Mas caso você queira ainda usar esse conceito de 12 colunas, pode usar também sem problema, é só utilizar a sintaxe `col-X-12` que o valor de X terá o mesmo resultado de você utilizar o col-x do Bootstrap. Legal, né?

Outra característica legal, é que pra você customizar a diagramação para vários tamanhos de tela, também ficou muito fácil. Como no exemplo que vimos ainda há pouco, temos 2 colunas, mas vamos supor que no celular eu quero uma coluna em cada linha e no tablet 2 colunas em 1 linha porém as duas do mesmo tamanho (lembrando que no desktop está pra aparecer 2/3 e 1/3 da tela). Ficaria assim:


```html 
<div class="cols">

    <div class="col-2-3 col-1-1-s1  col-1-2-col2">
        1º Coluna
    <div>
    <div class="col-1-3 col-1-1-s1 col-1-2-s3">
        2º Coluna
    <div>

</div>
````

Super fácil :)

---

## Boxes
Do que adianta você poder controlar a diagramação das colunas com simples classes se não consegue ter a mesma facilidade pra controlar os espaçamentos verticais.

Quem nunca passou pela situação onde você controla bem certinho as colunas, mas por exemplo no mobile o padding-top ficou mto grande? Agora ficou fácil de você controlar isso também. Veja como é simples a sintaxe:

```html
<div class="pad-l10"> ... </div>
```
No código acima, o resultado é um div com `padding-left` de `10px`. A sintaxe será sempre essa: `pad` + (`l`, `t`, `r` ou `b`)) + o número de pixels que você deseja que o `padding` tenha.

O mesmo funcionará para o `margin`, basta substituir na sintaxe o `pag` pelo `mar`. (Ex.: `mar-b20`)

E assim como nas colunas, você também consegue customizar para cada tamanho de tela:
```html
<div class="pad-t10 pad-t5-s1 pad-20-s2"> ... </div>
```

**Observação:** Por uma questão de performance e não deixar o framework pesado, você consegue utilizar espaçamentos multiplos de 5, em uma escala de 0 até 500.

---

## Plataformas

|  Nome         | Dispositivo           | Largura Mín.  | Largura Máx.  |
| ---           |---                    |---            |---            |
| **s1**        | Celular               |               | 768px         | 
| **s2**        | Tablet                |   769px       | 1023px        | 
| **s3**        | Computador            |  1024px       | 1215px        | 
| **s4**        | Monitor Widescreen    |  1216px       | 1407px        | 
| **s5**        | Grandes Resoluções    |  1408px       | ∞             | 
