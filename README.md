# Exercicio 1 JavaScript

// 1. Operações matemáticas básicas
function operacoesBasicas(num1, num2) {
    const soma = num1 + num2;
    const subtracao = num1 - num2;
    const multiplicacao = num1 * num2;
    const divisao = num1 / num2;

    console.log("Soma:", soma);
    console.log("Subtração:", subtracao);
    console.log("Multiplicação:", multiplicacao);
    console.log("Divisão:", divisao);
}

console.log("Operações matemáticas básicas:");
operacoesBasicas(10, 5);

// 2. Números ímpares de 0 a 100
console.log("\nNúmeros ímpares de 0 a 100:");
for (let i = 1; i <= 100; i += 2) {
    console.log(i);
}

// 3. Quantidade de caracteres
console.log("\nQuantidade de caracteres para o texto 'Disciplina de Programação para web':");
const texto = "Disciplina de Programação para web";
console.log(texto.length);

// 4. Formato de e-mail
function formatoEmail(nome) {
    const partesNome = nome.toLowerCase().split(" ");
    const primeiroNome = partesNome[0];
    const ultimoNome = partesNome[partesNome.length - 1];
    const email = primeiroNome + "." + ultimoNome + "@facens.br";
    return email;
}

console.log("\nFormato de e-mail:");
const nome = "Edson Martin Feitosa";
console.log(formatoEmail(nome));

// 5. Imprimir números de 1 a 10 com traço
console.log("\nNúmeros de 1 a 10 com traço:");
let numerosComTraco = "";
for (let i = 1; i <= 10; i++) {
    numerosComTraco += i;
    if (i !== 10) {
        numerosComTraco += " - ";
    }
}
console.log(numerosComTraco);

// 6. Função para mostrar o dobro do número
function dobroNumero(numero) {
    if (numero <= 0) {
        return "Só é aceito números positivos maiores que zero";
    } else {
        return numero * 2;
    }
}

// 7. Função para inverter uma string
function inverterString(string) {
    return string.split("").reverse().join("");
}

// 8. Função para contar vogais em uma string
function contarVogais(string) {
    const vogais = "aeiou";
    let count = 0;
    for (let char of string.toLowerCase()) {
        if (vogais.includes(char)) {
            count++;
        }
    }
    return count;
}

// 9. Função para verificar se um e-mail é válido
function validarEmail(email) {
    const partes = email.split("@");
    if (partes.length === 2 && partes[1].includes(".") && partes[1].indexOf(".") > partes[1].indexOf("@")) {
        return true;
    } else {
        return false;
    }
}

// 10. Função para verificar se uma string é um palíndromo
function verificarPalindromo(string) {
    return string === string.split("").reverse().join("");
}

// Testando as funções
console.log("\nTestando as funções:");
console.log("Dobro do número 5:", dobroNumero(5));
console.log("Inversão da string 'hello':", inverterString("hello"));
console.log("Número de vogais em 'hello':", contarVogais("hello"));
console.log("Validar e-mail 'test@example.com':", validarEmail("test@example.com"));
console.log("Verificar se 'arara' é um palíndromo:", verificarPalindromo("arara"));
