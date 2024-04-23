# Pedra-Papel-Tesoura-Lagarto-Spock
Um sistema bem basico sobre o jogo Pedra, Papel, Tesoura, Lagarto e Spock


from random import choice


jogador_vitorias = 0
maq_vitorias = 0


def opcao_jogador():
    "escolha de jogada"
    esc_jogador = input("Escolha Pedra, Papel, Tesoura, Lagarto ou Spock: ")
    esc_jogador.lower()
    if esc_jogador == "pedra":
        return esc_jogador
    if esc_jogador == "papel":
        return esc_jogador
    if esc_jogador == "tesoura":
        return esc_jogador
    if esc_jogador == "lagarto":
        return esc_jogador
    if esc_jogador == "spock":
        return esc_jogador
    opcao_jogador()


def opcao_maquina():
    "escolha de jogada da máquina"
    esc_maquina = choice(["pedra", "papel", "tesoura", "lagarto", "spock"])
    return esc_maquina


while True:

    print("-" * 30)
    esc_jogador = opcao_jogador()
    esc_maquina = opcao_maquina()
    print("-" * 30)

    if (
        (esc_jogador == "tesoura")
        and (esc_maquina == "papel")
        or (esc_jogador == "papel")
        and (esc_maquina == "pedra")
        or (esc_jogador == "pedra")
        and (esc_maquina == "lagarto")
        or (esc_jogador == "lagarto")
        and (esc_maquina == "spock")
        or (esc_jogador == "spock")
        and (esc_maquina == "tesoura")
        or (esc_jogador == "tesoura")
        and (esc_maquina == "lagarto")
        or (esc_jogador == "lagarto")
        and (esc_maquina == "papel")
        or (esc_jogador == "papel")
        and (esc_maquina == "spock")
        or (esc_jogador == "spock")
        and (esc_maquina == "pedra")
        or (esc_jogador == "pedra")
        and (esc_maquina == "tesoura")
    ):
        # jogador ganha
        print(
            f"Jogador escolheu: {esc_jogador} e a máquina: {esc_maquina}."
            " Resultado: Você Ganhou!"
        )
        jogador_vitorias += 1

    elif esc_jogador == esc_maquina:
        # empate
        print(
            f"Jogador escolheu: {esc_jogador} e a máquina: {esc_maquina}."
            " Resultado: Vocês Empataram!"
        )
    elif esc_jogador is None:
        # erro
        print("Erro, Encerrando Código...(Opçôes Escolhidas Inválidas)")
        break
    else:
        # máquina ganha
        print(
            f"Jogador escolheu: {esc_jogador} e a máquina: {esc_maquina}."
            " Resultado: Você Perdeu!"
        )
        maq_vitorias += 1
    print("-" * 30)
    print(f"Vitórias do Jogador: {jogador_vitorias}")
    print(f"Vitórias da Máquina {maq_vitorias}")
    print("-" * 30)

    esc_jogador = input("Você quer jogar novamente? ")
    if esc_jogador in ["SIM", "sim", "Sim", "s", "S"]:
        pass
    elif esc_jogador in ["NAO", "nao", "Nao", "n", "N"]:
        print("Jogo encerrado, obrigado por jogar! =))")
        print(50 * "-")
        break
    else:
        break
