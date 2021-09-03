import random

sala = 1
caminho = 0
tentativas = 0

while tentativas < 7 and sala < 10:
    tentativas = tentativas + 1
    print(f"Você está na sala: {sala}")
    print("Escolha seu caminho:")
    print("[1] - Caminho vermelho")
    print("[2] - Caminho preto")
    caminho = int(input())
    print()
    sala = sala + caminho
    if sala == 6:
        tentativas = tentativas + 1
        print(f"Você está na sala: {sala}")
        print("Siga apenas esse caminho:")
        print("[2] - Caminho preto")
        caminho = int(input())
        sala = sala + caminho
    elif sala == 9:
        print(f"Você está na sala: {sala}")
        print("Você ganhou. Parabéns.")
        break
    while sala == 10:
        x = random.randint(1,5)
        print(f"Você entrou no portal e foi para a casa {x}")
        print("Escolha seu caminho:")
        print("[1] - Caminho vermelho")
        print("[2] - Caminho preto")
        tentativas = tentativas + 1
        caminho = int(input()) 
        sala = sala + caminho
else:
    print("Suas tentativas acabaram. Tente novamente.")
