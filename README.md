# ac5
ac5
#1
def imprimir_texto(n):
    texto = """
    Esse é um exemplo de texto que você deseja imprimir.
    É possivel substituir este texto pelo seu próprio.
    Fique atento para manter a formatação correta.
    """

    linhas = texto.split('\n')

    for i in range(n):
        if i < len(linhas):
            print(linhas[i])

try:
    n = int(input("Insira o valor de n: "))
    imprimir_texto(n)
except ValueError:
    print("Por favor, insira um valor inteiro válido para n.")



#2
def contar_digitos(numero):
    num_str = str(numero)
    return len(num_str)

try:
    numero = int(input("Insira um número inteiro: "))
    quantidade_digitos = contar_digitos(numero)
    print(f"O número {numero} tem {quantidade_digitos} dígitos.")
except ValueError:
    print("Por favor, insira um número inteiro válido.")


#3

try:
    num1 = int(input("Insira o primeiro número inteiro: "))
    num2 = int(input("Insira o segundo número inteiro: "))
    resultado = num1 / num2
except ValueError:
    print("Erro: Cheque se o número inserido é um número inteiro válido.")
except ZeroDivisionError:
    print("Erro: Divisão por zero não é permitida.")
finally:
    try:
        print(f"Resultado da divisão: {resultado:.2f}")
    except NameError:
        print("Resultado não calculado por conta de erros anteriores.")
