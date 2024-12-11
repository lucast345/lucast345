def calculadora():
    print("Bem-vindo à calculadora!")
    print("Operações disponíveis:")
    print("1 - Soma (+)")
    print("2 - Subtração (-)")
    print("3 - Multiplicação (*)")
    print("4 - Divisão (/)")
    print("5 - Exponenciação (**)")
    
    while True:
        try:
            opcao = int(input("Escolha uma operação (1-5): "))
            if opcao not in [1, 2, 3, 4, 5]:
                print("Escolha uma opção válida.")
                continue

            num1 = float(input("Digite o primeiro número: "))
            num2 = float(input("Digite o segundo número: "))

            if opcao == 1:
                resultado = num1 + num2
                operacao = "+"
            elif opcao == 2:
                resultado = num1 - num2
                operacao = "-"
            elif opcao == 3:
                resultado = num1 * num2
                operacao = "*"
            elif opcao == 4:
                if num2 == 0:
                    print("Erro: divisão por zero não é permitida.")
                    continue
                resultado = num1 / num2
                operacao = "/"
            elif opcao == 5:
                resultado = num1 ** num2
                operacao = "**"
            
            print(f"O resultado de {num1} {operacao} {num2} é: {resultado}")
        except ValueError:
            print("Entrada inválida. Por favor, insira números válidos.")
        
        continuar = input("Deseja realizar outra operação? (s/n): ").lower()
        if continuar != 's':
            print("Encerrando a calculadora. Até mais!")
            break

# Chama a função calculadora
calculadora()
