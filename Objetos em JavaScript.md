# **Objetos em JavaScript**
---

## **1. Introdução aos Objetos**

Em JavaScript, um objeto é uma **estrutura de dados** usada para armazenar coleções de pares **chave-valor**. Ele permite organizar e manipular dados de forma estruturada.

### **Sintaxe básica**
A forma mais comum de criar um objeto é usando a **notação literal**:
```javascript
const objeto = {
  chave1: valor1,
  chave2: valor2
};
```

### Exemplo simples:
```javascript
const pessoa = {
  nome: "João",
  idade: 30,
  profissao: "Engenheiro"
};

console.log(pessoa.nome); // João
console.log(pessoa["idade"]); // 30
```

---

## **2. Propriedades em Objetos**

- **Propriedade** é uma associação entre uma chave (string ou símbolo) e um valor.
- O valor pode ser qualquer tipo: número, string, booleano, array, função ou até outro objeto.

### **Acessando Propriedades**
1. **Notação de ponto**:
   ```javascript
   console.log(pessoa.nome); // João
   ```
2. **Notação de colchetes**:
   ```javascript
   console.log(pessoa["idade"]); // 30
   ```

### **Adicionando/Modificando Propriedades**
```javascript
pessoa.altura = 1.75; // Adicionando nova propriedade
pessoa.idade = 31;    // Alterando valor existente
console.log(pessoa);
```

### **Removendo Propriedades**
```javascript
delete pessoa.profissao;
console.log(pessoa);
```

---

## **3. Métodos em Objetos**

Um método é uma função associada a uma propriedade de um objeto.

### **Exemplo de Objeto com Métodos**
```javascript
const pessoa = {
  nome: "Maria",
  saudacao: function() {
    return `Olá, meu nome é ${this.nome}`;
  }
};

console.log(pessoa.saudacao()); // Olá, meu nome é Maria
```

#### **Métodos abreviados** (sintaxe moderna)
```javascript
const calculadora = {
  somar(a, b) {
    return a + b;
  },
  subtrair(a, b) {
    return a - b;
  }
};

console.log(calculadora.somar(2, 3)); // 5
console.log(calculadora.subtrair(5, 2)); // 3
```

---

## **4. Iterando sobre Objetos**

### **Usando `for...in`**
```javascript
const produto = { nome: "Celular", preco: 1500, estoque: 50 };

for (let chave in produto) {
  console.log(`${chave}: ${produto[chave]}`);
}
// nome: Celular
// preco: 1500
// estoque: 50
```

### **Métodos úteis para objetos**
1. **`Object.keys()`**: Retorna um array com as chaves do objeto.
   ```javascript
   console.log(Object.keys(produto)); // ['nome', 'preco', 'estoque']
   ```

2. **`Object.values()`**: Retorna um array com os valores do objeto.
   ```javascript
   console.log(Object.values(produto)); // ['Celular', 1500, 50]
   ```

3. **`Object.entries()`**: Retorna um array de pares chave-valor.
   ```javascript
   console.log(Object.entries(produto)); 
   // [['nome', 'Celular'], ['preco', 1500], ['estoque', 50]]
   ```

---

## **5. Manipulando Objetos**

### **Clonando Objetos**
1. **Usando `Object.assign()`**:
   ```javascript
   const original = { a: 1, b: 2 };
   const copia = Object.assign({}, original);
   ```

2. **Usando o spread operator (`...`)**:
   ```javascript
   const copia = { ...original };
   ```

### **Mesclando Objetos**
```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };
const mesclado = { ...obj1, ...obj2 };
console.log(mesclado); // { a: 1, b: 2, c: 3, d: 4 }
```

---

## **6. Trabalhando com Referências**

Objetos são tipos de dados que funcionam por **referência**, não por valor.

### Exemplo:
```javascript
const a = { x: 10 };
const b = a;
b.x = 20;

console.log(a.x); // 20 (ambos apontam para o mesmo objeto)
```

### Solução: Criar cópias
Para evitar modificações não intencionais, use o spread operator ou `Object.assign()`.

---

## **7. Exercícios Resolvidos**

### **Exercício 1: Criar um objeto e acessar propriedades**
Crie um objeto chamado `carro` com as propriedades `marca`, `modelo` e `ano`. Acesse e exiba essas propriedades no console.

**Solução:**
```javascript
const carro = {
  marca: "Toyota",
  modelo: "Corolla",
  ano: 2021
};

console.log(carro.marca); // Toyota
console.log(carro.modelo); // Corolla
console.log(carro.ano); // 2021
```

---

### **Exercício 2: Adicionar e remover propriedades**
Crie um objeto chamado `livro` com as propriedades `titulo` e `autor`. Adicione a propriedade `ano` e depois remova `autor`.

**Solução:**
```javascript
const livro = {
  titulo: "JavaScript para Iniciantes",
  autor: "Fulano de Tal"
};

livro.ano = 2020; // Adicionando
delete livro.autor; // Removendo
console.log(livro); // { titulo: 'JavaScript para Iniciantes', ano: 2020 }
```

---

### **Exercício 3: Criar um método em um objeto**
Crie um objeto chamado `usuario` com a propriedade `nome` e um método `saudar()` que retorna a mensagem: `"Olá, meu nome é [nome]"`.

**Solução:**
```javascript
const usuario = {
  nome: "Ana",
  saudar() {
    return `Olá, meu nome é ${this.nome}`;
  }
};

console.log(usuario.saudar()); // Olá, meu nome é Ana
```

---

### **Exercício 4: Iterar sobre um objeto**
Crie um objeto chamado `aluno` com as propriedades `nome`, `idade` e `curso`. Use um `for...in` para exibir as chaves e valores.

**Solução:**
```javascript
const aluno = {
  nome: "Carlos",
  idade: 22,
  curso: "Engenharia"
};

for (let chave in aluno) {
  console.log(`${chave}: ${aluno[chave]}`);
}
// nome: Carlos
// idade: 22
// curso: Engenharia
```

---

## **8. Práticas Avançadas**

### **Congelar Objetos (`Object.freeze`)**
Impede alterações no objeto.
```javascript
const config = { api: "https://api.meusite.com" };
Object.freeze(config);

config.api = "https://api.hacker.com"; // Não funciona
console.log(config.api); // https://api.meusite.com
```

### **Selar Objetos (`Object.seal`)**
Impede a adição ou remoção de propriedades, mas permite modificar valores existentes.
```javascript
const usuario = { nome: "João" };
Object.seal(usuario);

usuario.nome = "Pedro"; // Funciona
delete usuario.nome; // Não funciona
usuario.idade = 25; // Não funciona
console.log(usuario); // { nome: "Pedro" }
```

---

## **Conclusão**

Agora você conhece os principais recursos do tipo de dado **objeto** no JavaScript. Com esses conceitos, você pode criar estruturas mais organizadas e flexíveis em seus programas. Continue praticando para dominar cada aspecto!
