# python-2

# classificador do cliente
"""
PORTUGOL (Pseudocódigo):


Algoritmo ClassificadorCliente
var
idade: Inteiro
renda: Real
Inicio
Escreva("Digite a idade do cliente: ")
Leia(idade)
Escreva("Digite a renda do cliente R$: ")
Leia(renda)


if (renda >= 10000) Então
  Escreva("Category: Diamante")
elif (renda >= 5000) Então
  Escreva("Category: Ouro")
elif (renda >= 2000) Então
  Escreva("Category: Prata")
else
  Escreva("Category: Bronze")
  fimse
  fim Algoritmo
  """
from unicodedata import category



print("Classificador de cliente")
idade = int(input("Digite a idade do cliente: "))
renda = float(input("Digite a renda do cliente R$: "))
if renda >= 10000:
    print("Category: Diamante")
elif renda >= 5000:
    print("Category: Ouro")
elif renda >= 2000:
    print("Category: Prata")
else:
    print("Category: Bronze")


print(f"Cliente com {idade} anos classificado na categoria: {categoria}")


#menu de operações matemáticas
"""
PORTUGOL (Pseudocódigo):
Algoritmo MenuOperacoesMatematicas
var
opcao: Inteiro
N1, N2, resultado: Real
INICIO
escreva(1-soma, 2-subtração, 3-multiplicação, 4-divisão)
Leia(opcao)
escolha(opcao)
caso 1: resultado <- N1 + N2
caso 2: resultado <- N1 - N2
caso 3: resultado <- N1 * N2
caso 4: resultado <- N1 / N2
outrocaso: escreva("Opção inválida")
fim escolha
fim Algoritmo
"""
print("Menu de operações matemáticas")
n1 = float(input("Digite o primeiro número: "))
n2 = float(input("Digite o segundo número: "))
print("Escolha a operação desejada:")
print("1 - Soma (+)")
print("2 - Subtração (-)")
print("3 - Multiplicação (*)")
print("4 - Divisão (/)")
opcao = int(input("Digite o número da operação desejada: "))
match opcao:
    case 1:
        resultado = n1 + n2
        print(f"O resultado da soma é: {resultado:.2f}")
    case 2:
        resultado = n1 - n2
        print(f"O resultado da subtração é: {resultado:.2f}")
    case 3:
        resultado = n1 * n2
        print(f"O resultado da multiplicação é: {resultado:.2f}")
    case 4:
        if n2 != 0:
            resultado = n1 / n2
            print(f"O resultado da divisão é: {resultado:.2f}")
        else:
            print("Erro: Divisão por zero não é permitida.")
    case _:
        print("Opção inválida!/n")





#análise de números
"""
PORTUGOL (Pseudocódigo):
Algoritmo AnaliseNumeros
var
i: Inteiro
num, soma,media,maior,menor: Real
Inicio
para i de 1 até 5 faça
leia(num)
soma <- soma + num
fim para
media <- soma / 5
fim Algoritmo
"""
print("Análise de números")
numeros = []
for i in range(1, 6):
    num = float(input(f"Digite o {i}º número: "))
    numeros.append(num)
soma_total = sum(numeros)
media_valores = soma_total / len(numeros)
maior_valor = max(numeros)
menor_valor = min(numeros)
print(f"A soma dos números é: {soma_total}")
print(f"A média dos números é: {media_valores:.2f}")
print(f"O maior número é: {maior_valor}")
print(f"O menor número é: {menor_valor}\n")



#sistema de autenticação
"""
PORTUGOL (Pseudocódigo):
Algoritmo SistemaAutenticacao
var
senha,tentativa: texto
tentativas,max_tentativas: Inteiro
Inicio
senha <- "1234"
tentativas <- 0
enquanto (tentativas <3) faça
leia(tentativa)
if (tentativa == senha) então interrompa
tentativas <- tentativas + 1
fim enquanto
fim Algoritmo
"""
print("Sistema de autenticação")
senha_correta = "1234"
max_tentativas = 3
tentativas = 0
acesso_concedido = False
while tentativas < max_tentativas:
    senha_digitada = input("Digite a senha: ")
    tentativas += 1
    if senha_digitada == senha_correta:
        acesso_concedido = True
        print(f"acesso permitido! (autenticando na {tentativas}ª tentativa)\n")
        break
    else:
     erros_restantes = max_tentativas - tentativas
     if erros_restantes > 0:
            print(f"Senha incorreta. Você tem {erros_restantes} tentativa(s) restante(s).\n")
     else:
            print("\nAcesso negado. Número máximo de tentativas atingido.\n")  
