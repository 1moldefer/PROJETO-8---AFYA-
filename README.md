# desafio 8 - cadastro de funcionarios

while True:
    print("\n=== CADASTRO DE FUNCIONARIOS (PADARIA DO SEU ZÉ)===")
 
    # for porque sei que sao 5 funcionarios, quantidade fixa
    for i in range(5):
        nome = input(f"\nFuncionario {i+1} de 5 - Nome: ").strip()
        print("Senha: 6 a 12 caracteres, maiuscula, minuscula e numero")

        tentativas = 0
        # while porque nao sei quantas tentativas o usuario vai precisar
        while True:
            tentativas += 1
            senha    = input("Senha: ").strip()
            confirma = input("Confirma: ").strip()

            erros = []
            if not senha:                              erros.append("senha vazia")
            elif len(senha) < 6:                       erros.append(f"minimo 6 caracteres (digitou {len(senha)})")
            elif len(senha) > 12:                      erros.append(f"maximo 12 caracteres (digitou {len(senha)})")
            if senha and not any(c.isupper() for c in senha): erros.append("falta maiuscula")
            if senha and not any(c.islower() for c in senha): erros.append("falta minuscula")
            if senha and not any(c.isdigit() for c in senha): erros.append("falta numero")
            if senha != confirma:                      erros.append("senhas diferentes")

            if erros:
                print("erro: " + ", ".join(erros))
            else:
                print(f"ok! {nome} cadastrado em {tentativas} tentativa(s)")
                break

    print("\ntodos cadastrados!")
    if input("\nENTER pra repetir ou S pra sair: ").strip().upper() == "S":
        print("encerrando...")
        break
