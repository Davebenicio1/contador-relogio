# contador-relogio
Relogio contador simples no py.

import time

def relogio_contador(segundos):
    while segundos:
        minutos, segs = divmod(segundos, 60)
        timer = f'{minutos:02}:{segs:02}'
        print(timer, end='\r')
        time.sleep(1)
        segundos -= 1
    print('Tempo esgotado!')

if __name__ == "__main__":
    tempo_inicial = int(input("Digite o tempo em segundos: "))
    relogio_contador(tempo_inicial)
