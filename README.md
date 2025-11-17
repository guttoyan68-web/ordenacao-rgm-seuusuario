# Projeto de Ordenação — RGM SEU_USUARIO  
Comparação entre Insertion Sort, Merge Sort e Quick Sort

---

## 📌 Descrição do Problema
O objetivo deste projeto é **ordenar os dígitos do RGM do aluno** em ordem crescente e, ao mesmo tempo, **comparar o desempenho de três algoritmos clássicos de ordenação**:

- **Insertion Sort**
- **Merge Sort**
- **Quick Sort**

A comparação é realizada tanto em **número de passos** quanto em **tempo de execução**, considerando diferentes tamanhos de entrada e três cenários:

- **Melhor caso**
- **Caso médio**
- **Pior caso**

Os dados coletados são exportados em formato **CSV** para análise posterior.

---

## 🧠 Métodos Implementados e Justificativa de Escolha

### 🔹 **1. Insertion Sort**
Escolhido por ser um algoritmo simples, intuitivo e eficiente em listas **pequenas** ou **quase ordenadas**.  
Complexidade:  
- Melhor caso: **O(n)**  
- Médio/pior caso: **O(n²)**  
Permite observar bem a diferença entre casos favoráveis e desfavoráveis.

### 🔹 **2. Merge Sort**
Representa algoritmos **O(n log n)** estáveis e com bom desempenho mesmo em casos adversos.  
É determinístico e não depende da disposição inicial da entrada.  
Complexidade:  
- Todos os casos: **O(n log n)**  
Teste ideal para comparar com Insertion e Quick.

### 🔹 **3. Quick Sort**
Escolhido por ser o algoritmo de ordenação **mais usado na prática**, com alto desempenho no caso médio.  
Complexidade:  
- Melhor/médio caso: **O(n log n)**  
- Pior caso: **O(n²)** (quando o pivô é ruim)  
Complementa a análise contrastando desempenho **teórico vs prático**.

---

## 🛠️ Como Compilar e Executar

Use **GCC** com otimização leve, conforme solicitado:

```bash
gcc -O1 -std=c11 src/*.c -o ordena
Para executar:

bash
Copiar código
./ordena
No Windows:

cmd
Copiar código
ordena.exe
A saída será registrada em:

bash
Copiar código
data/results.csv
📏 Política de Contagem de Passos
Para permitir comparação justa entre algoritmos, definiu-se:

+1 passo para cada comparação

+1 passo para cada troca ou movimentação de elemento

Todos os algoritmos usam a mesma métrica, permitindo comparação objetiva.

⏱️ Método de Medição de Tempo
Utiliza-se a função clock() da <time.h>, registrando:

tempo inicial

tempo final

diferença convertida para milissegundos

Cada teste é repetido 5 vezes, e o valor final gravado no CSV é a média.

📊 Resultados (média de 5 execuções)
O arquivo completo está em:

bash
Copiar código
/data/results.csv
Formato:

python-repl
Copiar código
algoritmo,N,caso,passos,tempo_ms
Merge,2000,medio,17500,0.21
Quick,2000,medio,15800,0.19
Insertion,2000,pior,1990000,22.35
...
