# Teste-Target-Sistemas
Questões de Desenvolvedor Back-End
 Primeira Questão:
 int INDICE = 13, SOMA = 0, K = 0;
while (K < INDICE) {
    K = K + 1;
    SOMA = SOMA + K;
}
Console.WriteLine(SOMA);
//Iterações do Loop:
Vamos simular as iterações do loop:

Iteração	Valor de K	Valor de SOMA
1	1	0 + 1 = 1
2	2	1 + 2 = 3
3	3	3 + 3 = 6
4	4	6 + 4 = 10
5	5	10 + 5 = 15
6	6	15 + 6 = 21
7	7	21 + 7 = 28
8	8	28 + 8 = 36
9	9	36 + 9 = 45
10	10	45 + 10 = 55
11	11	55 + 11 = 66
12	12	66 + 12 = 78
13	13	78 + 13 = 91
Fim do Loop:

Quando K atinge 13, a condição K < INDICE se torna falsa, e o loop termina.
======================================================================================================================================================
Segunda Questão:
Descobri um programa em Python
def is_fibonacci(n):
    a, b = 0, 1
    while a <= n:
        if a == n:
            return True
        a, b = b, a + b
    return False

# Entrada do usuário
num = int(input("Digite um número: "))

# Verificação e saída
if is_fibonacci(num):
    print(f"O número {num} pertence à sequência de Fibonacci.")
else:
    print(f"O número {num} NÃO pertence à sequência de Fibonacci.")
======================================================================================================================================================
Terceira Questão:
import json

# Exemplo de JSON com dados de faturamento
json_data = '''{
    "faturamento": [
        2210.50, 1843.20, 0, 0, 2450.75, 3100.60, 0,
        2750.10, 2890.50, 0, 0, 3200.85, 4100.90, 0,
        3900.10, 4000.75, 0, 0, 2800.60, 3100.40, 0,
        2600.90, 2950.30, 0, 0, 3300.20, 3600.90, 0,
        3700.60, 3850.70
    ]
}'''

# Carregar dados do JSON
dados = json.loads(json_data)
faturamento = [valor for valor in dados["faturamento"] if valor > 0]

# Cálculo do menor e maior valor de faturamento
menor_faturamento = min(faturamento)
maior_faturamento = max(faturamento)

# Cálculo da média mensal ignorando dias sem faturamento
media_mensal = sum(faturamento) / len(faturamento)

dias_acima_media = sum(1 for valor in faturamento if valor > media_mensal)

# Exibir resultados
print(f"Menor faturamento do mês: R$ {menor_faturamento:.2f}")
print(f"Maior faturamento do mês: R$ {maior_faturamento:.2f}")
print(f"Número de dias com faturamento acima da média: {dias_acima_media}")
=========================================================================================================================================================

Quarta Questão:
# Dados do faturamento mensal por estado
faturamento_estados = {
    "SP": 67836.43,
    "RJ": 36678.66,
    "MG": 29229.88,
    "ES": 27165.48,
    "Outros": 19849.53
}

# Cálculo do faturamento total
faturamento_total = sum(faturamento_estados.values())

# Exibir o percentual de cada estado
print("Percentual de representação por estado:")
for estado, valor in faturamento_estados.items():
    percentual = (valor / faturamento_total) * 100
    print(f"{estado}: {percentual:.2f}%")

Percentual de representação por estado:
SP: 37.53%
RJ: 20.31%
MG: 16.18%
ES: 15.03%
Outros: 10.96%
==================================================================================================================================================================

Quinta Questão:
# Solicita a string ao usuário
texto = input("Digite uma string para inverter: ")

# Inverte a string manualmente
string_invertida = ""
for i in range(len(texto) - 1, -1, -1):
    string_invertida += texto[i]

# Exibe o resultado
print(f"String invertida: {string_invertida}")

Digite uma string para inverter: Python
String invertida: nohtyP
