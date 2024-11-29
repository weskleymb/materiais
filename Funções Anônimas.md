## **Funções Anônimas e Arrow Functions em Algoritmos (JavaScript)**

### **1. Introdução às Funções Anônimas**

#### **O que são Funções Anônimas?**
- Funções que não possuem nome.
- Geralmente atribuídas a variáveis ou passadas como argumentos para outras funções.
- Muito úteis para algoritmos onde não é necessário reutilizar a função várias vezes.

**Exemplo:**
```javascript
const somar = function(a, b) {
    return a + b;
};
console.log(somar(5, 3)); // 8
```

---

### **2. Exemplos de Uso de Funções Anônimas**

#### **2.1. Função como uma variável**
```javascript
const multiplicar = function(a, b) {
    return a * b;
};
console.log(multiplicar(4, 5)); // 20
```

#### **2.2. Função como argumento de outra função**
Funções anônimas são muito usadas em algoritmos para passar comportamentos personalizados.

**Exemplo:**
```javascript
function executarOperacao(a, b, operacao) {
    return operacao(a, b);
}

const resultado = executarOperacao(10, 5, function(a, b) {
    return a - b;
});
console.log(resultado); // 5
```

#### **2.3. Como Função Imediata (IIFE)**
Uma função anônima pode ser executada imediatamente após ser declarada.

**Exemplo:**
```javascript
const resultado = (function() {
    return 10 * 2;
})();
console.log(resultado); // 20
```

---

### **3. Introdução às Arrow Functions**

#### **O que são Arrow Functions?**
- Uma forma mais curta e moderna de declarar funções anônimas.
- Usam a sintaxe `=>` (fat arrow).
- São especialmente úteis em algoritmos curtos e para simplificar o código.

**Sintaxe Básica:**
```javascript
const somar = (a, b) => a + b;
console.log(somar(4, 6)); // 10
```

#### **Por que usar Arrow Functions?**
- Reduzem a quantidade de código necessário.
- Eliminam a necessidade da palavra-chave `function`.
- Para expressões simples, não exigem `{}` ou `return`.

**Exemplo com retorno implícito:**
```javascript
const dobrar = numero => numero * 2;
console.log(dobrar(7)); // 14
```

---

### **4. Exemplos de Arrow Functions em Algoritmos**

#### **4.1. Operações Matemáticas**
```javascript
const subtrair = (a, b) => a - b;
console.log(subtrair(15, 5)); // 10
```

#### **4.2. Trabalhando com Arrays**
**Dobrar os números de um array:**
```javascript
const numeros = [1, 2, 3, 4];
const dobrados = numeros.map(numero => numero * 2);
console.log(dobrados); // [2, 4, 6, 8]
```

**Filtrar números pares:**
```javascript
const numeros = [1, 2, 3, 4, 5, 6];
const pares = numeros.filter(numero => numero % 2 === 0);
console.log(pares); // [2, 4, 6]
```

**Soma dos números de um array:**
```javascript
const numeros = [1, 2, 3, 4];
const soma = numeros.reduce((acumulador, numero) => acumulador + numero, 0);
console.log(soma); // 10
```

#### **4.3. Funções com Retorno de Objetos**
**Criar objetos de forma simplificada:**
```javascript
const criarPessoa = (nome, idade) => ({ nome, idade });
console.log(criarPessoa("Ana", 30)); // { nome: 'Ana', idade: 30 }
```

---

### **5. Exercícios Resolvidos**

#### **Exercício 1: Soma com Função Anônima**
**Problema:** Crie uma função anônima que retorne a soma de dois números.

**Solução:**
```javascript
const soma = function(a, b) {
    return a + b;
};
console.log(soma(8, 12)); // 20
```

---

#### **Exercício 2: Dobrar números com Arrow Function**
**Problema:** Use uma arrow function para dobrar os números de um array.

**Solução:**
```javascript
const numeros = [2, 4, 6, 8];
const dobrados = numeros.map(numero => numero * 2);
console.log(dobrados); // [4, 8, 12, 16]
```

---

#### **Exercício 3: Filtrar números maiores que 10**
**Problema:** Filtre os números maiores que 10 de um array.

**Solução:**
```javascript
const numeros = [5, 12, 18, 7, 3];
const maiores = numeros.filter(numero => numero > 10);
console.log(maiores); // [12, 18]
```

---

#### **Exercício 4: Soma dos Quadrados**
**Problema:** Calcule a soma dos quadrados dos números em um array.

**Solução:**
```javascript
const numeros = [1, 2, 3];
const somaQuadrados = numeros.reduce((acumulador, numero) => acumulador + numero ** 2, 0);
console.log(somaQuadrados); // 14
```

---

### **6. Desafios para Prática**

#### **Desafio 1: Multiplicar elementos de dois arrays**
Crie uma função que receba dois arrays e retorne um novo array com os elementos correspondentes multiplicados.

**Exemplo:**
- Entrada: `[1, 2, 3]`, `[4, 5, 6]`
- Saída: `[4, 10, 18]`

**Solução Sugerida:**
```javascript
const multiplicarArrays = (array1, array2) => array1.map((num, i) => num * array2[i]);
console.log(multiplicarArrays([1, 2, 3], [4, 5, 6])); // [4, 10, 18]
```

---

#### **Desafio 2: Filtrar palavras curtas**
Dado um array de palavras, filtre as que possuem menos de 4 letras.

**Exemplo:**
- Entrada: `["sol", "lua", "estrela", "mar"]`
- Saída: `["sol", "lua", "mar"]`

**Solução Sugerida:**
```javascript
const palavras = ["sol", "lua", "estrela", "mar"];
const curtas = palavras.filter(palavra => palavra.length < 4);
console.log(curtas); // ["sol", "lua", "mar"]
```

---

#### **Desafio 3: Média dos números de um array**
Crie uma função que calcule a média dos números de um array.

**Exemplo:**
- Entrada: `[10, 20, 30, 40]`
- Saída: `25`

**Solução Sugerida:**
```javascript
const calcularMedia = numeros => numeros.reduce((soma, num) => soma + num, 0) / numeros.length;
console.log(calcularMedia([10, 20, 30, 40])); // 25
```

---

### **7. Resumo**

1. **Funções Anônimas:**
   - Não possuem nome.
   - São úteis para algoritmos onde a reutilização do código não é necessária.

2. **Arrow Functions:**
   - Tornam o código mais conciso.
   - Elimina `function` e, em expressões simples, `{}` e `return`.

3. **Uso em Algoritmos:**
   - Ideal para operações em arrays como `map`, `filter` e `reduce`.
   - Simplificam operações matemáticas, filtros e cálculos agregados.

