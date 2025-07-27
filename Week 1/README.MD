# Conceitos Básicos em R - Introdução  

Este resumo contém materiais introdutórios para aprender **R**, abordando **operadores**, **estruturas condicionais** e **estruturas de repetição (loops)**.

---

## 📌 **Operadores em R**  

### 1. **Operadores Aritméticos**  
Usados para cálculos matemáticos básicos.  

```r
x <- 10  
y <- 3  

x + y   # Soma → 13  
x - y   # Subtração → 7  
x * y   # Multiplicação → 30  
x / y   # Divisão → ~3.33  
x ^ y   # Potência → 1000  
x %% y  # Módulo (resto da divisão) → 1  
x %/% y # Divisão inteira → 3  
```

### 2. **Operadores Relacionais**  
Comparam valores e retornam `TRUE` ou `FALSE`.  

```r
x > y   # Maior que → TRUE  
x <= y  # Menor ou igual → FALSE  
x == y  # Igualdade → FALSE  
x != y  # Diferente → TRUE  
```

### 3. **Operadores Lógicos**  
Usados para combinar condições.  

```r
a <- TRUE  
b <- FALSE  

a & b   # AND (E) → FALSE (ambos precisam ser TRUE)  
a | b   # OR (OU) → TRUE (apenas um precisa ser TRUE)  
!a      # NOT (NEGAÇÃO) → FALSE  
```

---

## 🔄 **Estruturas Condicionais**  

### 1. **`if-else` (Se-Senão)**  
Executa um bloco de código **se** uma condição for atendida.  

```r
nota <- 8.5  

if (nota >= 7) {  ## Eecuta o if se ele for true
  print("Aprovado!")  
} else {  ## caso o if for false executa o else
  print("Reprovado.")  
}  
```

### 2. **`ifelse()` (Versão Vetorizada)**  
Aplica uma condição em **vetores** sem precisar de loops.  

```r
notas <- c(6.5, 8, 4.3)  
resultado <- ifelse(notas >= 7, "Aprovado", "Reprovado")  
print(resultado)  # Saída: "Reprovado" "Aprovado" "Reprovado"  
```

### 3. **`switch()` (Escolha-Caso)**  
Útil para múltiplas condições baseadas em um valor.  

```r
dia <- "Segunda"  

switch(dia,  
       "Segunda" = print("Começo da semana"),  
       "Sexta"   = print("Quase fim de semana!"),  
       print("Dia comum.")  # Caso padrão  
)  
```

---

## 🔁 **Estruturas de Repetição (Loops)**  

### 1. **`for` (Para)**  
Repete um bloco de código um **número fixo** de vezes.  

```r
for (i in 1:5) {  
  print(paste("Iteração", i))  
}  
```

### 2. **`while` (Enquanto)**  
Repete um bloco **enquanto** uma condição for verdadeira.  

```r
contador <- 1  
while (contador <= 3) {  
  print(paste("Contagem:", contador))  
  contador <- contador + 1  
}  
```

### 3. **`repeat` + `break`**  
Repete **indefinidamente** até que `break` seja acionado.  

```r
valor <- 1  
repeat {  
  print(valor)  
  valor <- valor + 1  
  if (valor > 3) break  # Interrompe o loop  
}  
```

---

## 📚 **Referências**  
- [Documentação Oficial do R](https://www.r-project.org/)  

--- 

Contribuições são bem-vindas! Sinta-se à vontade para abrir **issues** ou **pull requests**. 🚀  

--- 

Espero que ajude! Adapte conforme necessário. 😊
