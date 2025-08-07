menu = """======= Menu =======

[1] Depositar
[2] Sacar
[3] Extrato
[0] Sair
====================

=> """

saque = 0
valor = 0
saldo = 0
limite = 500
extrato = ""
numero_saque = 0
LIMITE_SAQUES = 3

while True:

    opcao = input(menu)

    if opcao == "1":
        print("\n---Depósito---\n")
        valor = float(input("Digite o valor que deseja depositar: R$"))
        if  valor <= 0:
            print("Valor inválido! Por favor tente novamente.")
        
        elif valor >= 1:
            saldo += valor
            extrato += f"\nDepósito: R$ {valor: .2f}\n"
            print("Depósito realizado com sucesso!\n")
            print(f"Seu saldo foi atualizado para R${valor: .2f}\n\n")
        else:
            print("""\n     ### ERRO ### 
Digite um valor válido!\n""")
            
    elif opcao == "2":
        print("\n---Saque---\n")
        print(f"Seu saldo é de R${saldo: .2f}\n")
        saque = float(input("""Digite o valor que deseja sacar:
=> R$ """))
        if numero_saque >= LIMITE_SAQUES:
            print(f"\nLimite de saques diarios alcançado!\n")
        
        elif saque > limite:
            print("\nValor de saque maior que o limite, digite outro valor!\n")
            
        elif saque <= 0:
            print("\nValor inválido! Digite um valor positivo.\n")

        else:
            saldo -= saque
            extrato += f"Saque:     R$ {saque:.2f}\n"
            numero_saque +=1
            print(f"\nSaque realizado com sucesso! Seu saldo é de R${saldo: .2f}\n")
            

    elif opcao == "3":
        print("\n------Extrato------")
        if extrato == "":
            print("Não foram realizadas movimentações hoje.\n")

        else:
            print(extrato)
        print(f"Saldo atual: R${saldo:.2f}")
        print("--------------------")
        
    elif opcao == "0":
        print("\nSistema encerrado, tenha um ótimo dia.\n")
        break

    else:
        print("Operação inválida, por favor selecione novamente a operação desejada.")
