
# P2c — Condições de Corrida com e sem Mutex

**Universidade Federal do Maranhão (UFMA)**  
**Disciplina:** Sistemas Operacionais — 2026.2  
**Equipe:** 6  
**Tema T2:** Condições de corrida com e sem mutex

## 1. Integrantes

- Antonio Marcos Patrício Castro
- Jeysraelly Almone da Silva
- Kely Souza da Silva
- Pedro Lucas Machado Tavares
- Vinicius Bastos Amaral

## 2. Sobre o projeto

Este repositório reúne os materiais desenvolvidos para a atividade P2c da disciplina de Sistemas Operacionais.

O trabalho investiga condições de corrida em um contador compartilhado, comparando seu comportamento em execuções sem sincronização e com o uso de mutex.

O experimento utiliza uma simulação lógica em Python, desenvolvida a partir do caderno-modelo oficial disponibilizado pelo professor.

A atividade corresponde a 60% da nota da segunda avaliação (P2), equivalente a 6,0 pontos.

## 3. Objetivo

Analisar a quantidade média de incrementos perdidos quando diferentes threads disputam o acesso a um contador compartilhado e verificar em que medida a utilização de mutex elimina essas perdas.

**Pergunta de pesquisa:**

Qual é a quantidade média de incrementos perdidos em um contador compartilhado por 2, 4 e 8 threads sem sincronização, e em que medida a utilização de mutex elimina essas perdas?

## 4. Metodologia

A simulação considera um contador compartilhado, no qual cada incremento é dividido em três operações:

- **LOAD:** leitura do valor do contador.
- **ADD:** adição de uma unidade ao valor lido.
- **STORE:** escrita do resultado no contador.

São comparados dois cenários:

1. **Sem mutex:** as operações das threads podem ser intercaladas, provocando condições de corrida.
2. **Com mutex:** a seção crítica é protegida, impedindo que duas threads realizem simultaneamente as operações de incremento.

### Configurações do experimento

| Parâmetro | Configuração |
|---|---|
| Número de threads | 2, 4 e 8 |
| Incrementos por thread | 100 |
| Sementes pseudoaleatórias | 0 a 19 |
| Repetições por cenário | 20 |
| Cenários | Com e sem mutex |
| Total de simulações | 120 |

### Métricas analisadas

- Média de incrementos perdidos.
- Percentual de incrementos perdidos.
- Média de passos lógicos executados.

Os resultados são apresentados em tabela e gráficos, permitindo comparar a consistência do contador e a quantidade de passos necessária em cada cenário.

**Observação:** o experimento é uma simulação lógica. Os passos contabilizados não representam diretamente o tempo de execução ou o desempenho real de threads em um sistema operacional.

## 5. Estrutura do repositório

```text
so-p2c-t2/
├── notebook/
│   └── P2c_T2_caderno.ipynb
├── artigo/                  # Artigo final em PDF
├── .gitignore
└── README.md
```

A pasta `artigo/` será utilizada para armazenar a versão final do mini-artigo, caso ainda não tenha sido adicionada ao repositório.

## 6. Execução do notebook

O notebook pode ser aberto diretamente no Google Colab:

[**Abrir notebook no Google Colab**](https://colab.research.google.com/github/Jeys-almone/so-p2c-t2/blob/main/notebook/P2c_T2_caderno.ipynb)

Para reproduzir o experimento:

1. Abra o notebook pelo link acima.
2. No Colab, selecione **Ambiente de execução > Executar tudo**.
3. Aguarde a conclusão das células.
4. Confira os testes automáticos, a tabela e os gráficos.
5. Verifique se os resultados correspondem aos parâmetros definidos no experimento.

O notebook utiliza Python, Matplotlib e bibliotecas da instalação padrão do Python.

## 7. Organização do trabalho

O GitHub é utilizado para armazenar os arquivos, acompanhar alterações e facilitar a colaboração entre os integrantes.

Antes de começar uma alteração, atualize sua cópia local:

```bash
git pull
```

Depois de concluir e revisar as modificações:

```bash
git add .
git commit -m "Descreva a alteração realizada"
git push
```

Para evitar conflitos, recomendamos que apenas uma pessoa edite o notebook por vez, comunicando previamente as alterações ao restante da equipe.

### Salvando alterações feitas no Colab

No menu do Google Colab, selecione:

**Arquivo > Salvar uma cópia no GitHub**

Informe:

- **Repositório:** `Jeys-almone/so-p2c-t2`
- **Branch:** `main`
- **Caminho:** `notebook/P2c_T2_caderno.ipynb`

Confirme o salvamento e verifique a versão atualizada no GitHub.

## 8. Entrega da atividade

**Prazo:** sábado, 21 de novembro de 2026, às 23h59.

Materiais previstos:

- Mini-artigo final em PDF.
- Notebook oficial T2 completo e executado.
- Link compartilhável do notebook no Google Colab.

A entrega deverá seguir as orientações da atividade no SIGAA.

## 9. Considerações finais

O projeto busca demonstrar, por meio de uma simulação reproduzível, como a ausência de sincronização pode comprometer a consistência de dados compartilhados e como a exclusão mútua pode evitar a perda de atualizações.

O material também servirá de apoio à discussão dos resultados no mini-artigo.

---

**UFMA — Sistemas Operacionais — Equipe 6 — 2026.2**
