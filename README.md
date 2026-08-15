## Nivel 1: O Básico da Investigação
O que o código faz?
a funbção analisar() é alimentada por um texto/informação e realiza a verificação da informação se é ou não um palindromo.
para isso ele remove todas as informações ( virgula, "-", tudo que não é letra nem numeros)
inverte o textp 
faz uma comparação entre os textos.
if os dois forem iguais = true
caso contrario = false

remove caracteres especiais
remove espaços
converte para minúsculas
STRING LIMPA
inverte
compara

re.sub() - remove caracteres que nao são alfanuméricos.

.lower() - transforma caracteres em minusculo

[::-1] - inverte

== - compara

return - volta o resultado 

Como executar?

salve o arquivo .py 

executar o comando; python DesafioLogica.py

saidas:

False

true

## Nivel 2 Engenharia Reversa e Análise de Comportamento

função do main;
no python faz o codigo seja executado quando o arquivo abrir automaticamente.

explicando o: 
método analisar(String entrada) 

recebe uma frase e verifica se ela é um palíndromo (palíndromo uma palavra ou frase que continua igual quando é possivel ler de trás para frente, desconsiderando espaços, pontuação etc.)

ex:

texto1 = "A sacada da casa de cadasa"

= asadecadasecadadacasa
=false

texto2 = "Socorram-me, subi no ônibus em Marrocos"

= Socorrammesubinoonibusemmarrocos
=true

## Código

import re

def analisar(entrada):
    if entrada is None:
        return False
    
    # Remove tudo que não for letra ou número e converte para minúsculas
    limpa = re.sub(r'[^a-zA-Z0-9]', '', entrada).lower()
    
    # Inverte a string usando fatiamento (slicing)
    invertida = limpa[::-1]
    
    return limpa == invertida

if __name__ == "__main__":
    texto1 = "A sacada da casa de cadasa"
    texto2 = "Socorram-me, subi no ônibus em Marrocos"

    print(f"Teste 1: {analisar(texto1)}")
    print(f"Teste 2: {analisar(texto2)}")
