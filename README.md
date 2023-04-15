import random

# Imprime as opções disponíveis
print("Opções:\n1 - Pedra\n2 - Papel\n3 - Tesoura")

# Obtem a escolha do jogador
jogador = int(input("Escolha sua opção (1-3): "))

# Verifica se a escolha é válida
if jogador < 1 or jogador > 3:
    print("Escolha inválida!")
else:
    # Imprime a escolha do jogador
    if jogador == 1:
        print("Jogador escolheu Pedra.")
    elif jogador == 2:
        print("Jogador escolheu Papel.")
    else:
        print("Jogador escolheu Tesoura.")

    # Obtem a escolha do computador
    computador = random.randint(1, 3)

    # Imprime a escolha do computador
    if computador == 1:
        print("Computador escolheu Pedra.")
    elif computador == 2:
        print("Computador escolheu Papel.")
    else:
        print("Computador escolheu Tesoura.")

    # Verifica quem ganhou
    if jogador == computador:
        print("Empate!")
    elif jogador == 1 and computador == 3:
        print("Jogador venceu!")
    elif jogador == 2 and computador == 1:
        print("Jogador venceu!")
    elif jogador == 3 and computador == 2:
        print("Jogador venceu!")
    else:
        print("Computador venceu!")
