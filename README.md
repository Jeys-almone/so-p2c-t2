# P2c - Mini-artigo de Sistemas Operacionais (2026.2)

**Tema T2:** condição de corrida com e sem mutex.

## Equipe

- Antonio Marcos Patrício Castro
- Jeysraelly Almone da Silva
- Kely Souza da Silva
- Pedro Lucas Machado Tavares
- Vinicius Bastos Amaral


## A atividade

A P2c vale 6,0 pontos da 2ª avaliação. A gente precisa comparar duas formas de atualizar um contador compartilhado entre várias threads: sem proteção nenhuma e com mutex. A comparação é feita por uma simulação em Python no Colab, variando o número de threads (2, 4 e 8) e medindo quantos incrementos se perdem e quantos passos cada versão gasta.

- **Alternativas comparadas:** contador compartilhado sem e com mutex
- **Parâmetro variado:** número de threads
- **Métricas:** incrementos perdidos e passos executados

**Entrega:** PDF do artigo + link do Colab, até sábado, 21/11, às 23h59.

## O que vamos entregar

- **Notebook** (`notebook/P2c_T2_caderno.ipynb`): a simulação, com o link do Colab
- **Artigo** (`artigo/`): o texto final em PDF

## Pra que serve este repositório

Versionamento dos arquivos do trabalho, para a equipe sempre partir da versão mais atual.
## Como trabalhar

Antes de começar, puxe a versão mais nova. Quando terminar, envie a sua.

```
git pull
# ... edita ...
git add .
git commit -m "o que você mudou"
git push
```

O notebook é editado por uma pessoa de cada vez. O arquivo `.ipynb` não se mistura bem quando duas pessoas mexem ao mesmo tempo, então avise no grupo antes de abrir e quando der push.

## Ambiente

O notebook é desenvolvido no VS Code e entregue pelo Colab.

O link do Colab abre a versão mais recente do repositório:

https://colab.research.google.com/github/Jeys-almone/so-p2c-t2/blob/main/notebook/P2c_T2_caderno.ipynb

Para devolver alterações feitas no Colab: Arquivo > Salvar uma cópia no GitHub.
