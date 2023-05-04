'''
o usuário irá inserir o seu cpf e através do calculo de algoritmo de geração de cpf 
os útimos dois digitos serão calculados e com base neles determinado se o cpf é válido ou não
'''
import re

#input para receber o cpf e remover pontos e traços
cpf = input('Digite o seu cpf ')
cpf = re.sub('[^0-9]', '', cpf)

#condicional para tratar erros
if len(cpf) > 11: 
    print('CPF digitado inválido.')
#tratamento para saber se o que foi digitado pelo usuário são caracteres repetidos

for caractere in cpf:
    tratamento = ''
    tratamento = caractere * len(cpf)
    if tratamento == cpf:
        print('o cpf inserido é inválido devido aos caracteres serem repetidos. ')
        break

#contagem para saber o penúltimo digito
nove_digitos = cpf[:9]
contador_regressivo = 10
resultado = 0
primeiro_digito = 0
#calcular o primeiro digito 

for digito in nove_digitos: 
    resultado = resultado + (int(digito) * contador_regressivo)
    contador_regressivo -= 1
   
resultado = resultado * 10 

resultado = resultado % 11
if resultado <= 9:
    resultado = resultado 
else: 
    resultado = 0
gerado1 = str(nove_digitos) + str(resultado)

#calcular o último digito 
contador_regressivo_2 = 11
resultado2 = 0
segundo_digito = 0

for digitodois in gerado1:
    resultado2 += int(digitodois) * contador_regressivo_2
    contador_regressivo_2 -= 1

resultado2 = resultado2 * 10
resultado2 = resultado2 % 11

if resultado2 <= 9:
    resultado2 = resultado2

else: 
    resultado2 = 0

cpf_gerado = str(gerado1) + str(resultado2)


if cpf == cpf_gerado: 
    print(f'O cpf {cpf} é válido')
else: 
    print(f'O cpf: {cpf} é invalido')

