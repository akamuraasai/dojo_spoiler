# The Spoiler Escape

Uma página de facebook com o tema de super herois, posta diversas imagens com memes e referências a filmes e quadrinhos. Você ainda não viu Vingadores: Guerra Infinita e não quer tomar spoiler, e conhece uma IA que analisa imagens e define se ela possui spoiler ou não, baseado num valor de 0 a 100. Seu objetivo é validar se você pode ou não acessar os conteúdos desta página no dia de hoje.

## Descrição

Neste exercicio existirá um conjunto de imagens com nomes e valores de 0 a 100, um valor abaixo de 40 significa que a imagem não possui spoilers. Entre 41 e 65 a imagem possui um spoiler fraco/irrelevante. Entre 66 e 85 a imagem possui um spoiler, mas fora de contexto. e acima de 85 a imagem possui um forte spoiler.
Você não deve visitar a página caso haja algum spoiler forte.
Você não deve visitar a página caso haja 70% ou mais de spoilers fora de contexto.
Você não deve visitar a página caso haja 40% de spoilers fracos/irrelevantes e 40% de spoilers fora de contexto.
Em qualquer outro caso, você pode visitar a página normalmente sem se preocupar em sair frustrado dela.

## Testcases

### Input #0 (CRITICO)
```python
imagens = {
  'img1.jpg': 38,
  'img2.jpg': 33,
  'img3.jpg': 25,
  'img4.jpg': 11,
  'img5.jpg': 90,
  'img6.jpg': 14,
}
```

### Output #0
```
NAO VISITAR
```

### Input #1 (70%)
```python
imagens = {
  'img1.jpg': 38,
  'img2.jpg': 33,
  'img3.jpg': 67,
  'img4.jpg': 71,
  'img5.jpg': 85,
  'img6.jpg': 69,
  'img7.jpg': 69,
  'img8.jpg': 71,
  'img9.jpg': 81,
  'img10.jpg': 14,
}
```

### Output #1
```
NAO VISITAR
```

### Input #2 (40%/40%)
```python
imagens = {
  'img1.jpg': 38,
  'img2.jpg': 53,
  'img3.jpg': 62,
  'img4.jpg': 71,
  'img5.jpg': 85,
  'img6.jpg': 53,
  'img7.jpg': 49,
  'img8.jpg': 71,
  'img9.jpg': 81,
  'img10.jpg': 14,
}
```

### Output #2
```
NAO VISITAR
```

### Input #3 (40%/30%)
```python
imagens = {
  'img1.jpg': 38,
  'img2.jpg': 53,
  'img3.jpg': 62,
  'img4.jpg': 71,
  'img5.jpg': 85,
  'img6.jpg': 53,
  'img7.jpg': 49,
  'img8.jpg': 71,
  'img9.jpg': 11,
  'img10.jpg': 14,
}
```

### Output #3
```
PODE VISITAR
```