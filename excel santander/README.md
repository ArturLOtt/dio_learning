# dio_learning
repositório com trabalhos aprendidos pela plataforma de ensino DIO

# PERGUNTAS: Dados e Inteligência Artificial

1) As perguntas que a ferramenta responde, e onde aparece cada resposta;

2) Como o VF e o PROCV entram nos cálculos;

3) Os intervalos nomeados que você criou;

4) Os percentuais de cada perfil, e de onde vieram;

5) O que você mudou em relação à ferramenta do Expert.

## RESPOSTAS

1) A ferramenta responde com que frequencia se investir (mêses, anos) e se calcula a quantidade de retorno esperado.

2) O VF calcula o montante acumulado no futuro com base em aportes recorrentes e uma taxa de juros mensal constante. Formula =FV(taxa_mensal, qtd_anos*12, aporte*-1)
 O PROCV  é usado para buscar o percentual de alocação recomendado para cada tipo de FII combinando o perfil de investidor selecionado e a categoria do fundo. Formula =VLOOKUP($C$32&"-"&B36, Planilha2!$A:$D, 4, FALSE)

3)
$D$12 (Valor do salário base)
$D$13 (Percentual de rendimento mensal estimado para os dividendos)
$D$14 (Cálculo do valor sugerido para investimento com base no salário)
$D$17 (Valor mensal efetivamente investido)
$D$18 (Período em anos do plano)
$D$19 (Taxa de rendimento mensal adotada nos cálculos)
$D$20 (Patrimônio total acumulado calculado pela função VF)

4)
###Perfil Conservador:

Papel: 30%
Tijolo: 50%
Híbridos: 10%
FOFs: 10%
Desenvolvimento: 0%
Hotelarias: 0%

###Perfil Moderado:

Papel: 32%
Tijolo: 35%
Híbridos: 8%
FOFs: 5%
Desenvolvimento: 10%
Hotelarias: 10%

###Perfil Agressivo:

Papel: 50%
Tijolo: 10%
Híbridos: 5%
FOFs: 5%
Desenvolvimento: 20%
Hotelarias: 10%

5) A planilha permite alterações nas células específicas para atualizar automaticamente todo o restante do modelo:
C23 altera o perfil do investidor (conservador, moderado, agressivo)
D17 para se modificar o aporte mensal
D18 para se modificar a quantidade de anos
D19 para se modificar a taxa de rendimento mensal

-----

✍️ *Desenvolvido por Artur L.Ott*  
🔗 https://www.linkedin.com/in/artur-locateli-ott-57bbb1a9/ | https://github.com/ArturLOtt
