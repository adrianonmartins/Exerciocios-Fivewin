#Include"Fivewin.ch"
*******************
Function main()
*******************   
	Exercicio43()
*******************
return nil

Function Exercicio31()
Local nInt := 0.00

MsgGet("Exercicio 3.1","Informe seu numero",@nInt)
MsgInfo(nInt+5,"Resultado")

Return Nil

Function Exercicio32()
Local nInt := 0.00

MsgGet("Exercicio 3.2","Informe seu numero",@nInt)
MsgInfo(nInt*2,"Resultado")

Return Nil

Function Exercicio33()
Local nInt:= 0
Local nInt2:= 0
MsgGet("Exercicio 3.3","Informe a data de Nascimento Com 4 Digitos:",@nInt)
nInt2:= 2012 - nInt
MsgInfo(nInt2,"Sua Idade em 2012 era:","Idade")

Return Nil

Function Exercicio34()
Local nNota1:= 0
Local nNota2:= 0
Local nMedia:= 0

MsgGet("Exercicio 3.4","Informe a Primeira nota",@nNota1)
MsgGet("Exercicio 3.4","Informe a Primeira nota",@nNota2)

nMedia:= (nNota1+nNota2)/2

MsgInfo(nMedia,"Sua Média Final é:")
Return Nil

Function Exercicio35()
Local nRaio:=0
Local nPi:=3.14
Local nComprimento:=0

MsgGet("Exercicio 3.5","Informe o Valor do Raio",@nRaio)
nComprimento:= (2*nPi)*nRaio

MsgInfo(nComprimento,"O Coprimento total é de:")



Return Nil

Function Exercicio36()

Return Nil

Function Exercicio37()

Return Nil

Function Exercicio38()

Return Nil

*******  EXERCICIO 4.1 *********
    Function Exercicio41()
********************************
    local nNumero1  
      nNumero1:= 0.00
       msgget("Exercicio 04.1","Informe o numero",@nNumero1,)

       MsgInfo(STR((nNumero1*nNumero1),10,2),"Resultado do Numero ao Quadrado")
       MsgInfo(nNumero1^2,"Resultado do Numero ao Quadrado")
       MsgInfo(SQRT(nNumero1),"Raiz Quadrada")
       MsgInfo(STR(Int(nNumero1),10,2),"Parte Inteira do Numero")
       MsgInfo(Mod(nNumero1),"Parte Fracionaria")

     Return nil 

******* EXERCICIO 4.2 **********
    Function Exercicio42()
********************************
       Local kmInicial           
       Local kmFinal          
       Local qtdLtGasto         
       Local precoLtCombt          
       Local cptanque
       Local kmPorLitro
       Local custoViagem

       kmInicial:= 0.00          
       kmFinal:= 0.00          
       qtdLtGasto:= 0.00          
       precoLtCombt:= 0.00          
       cptanque:= 0.00

       MsgGet("Exercicio 4.2","Informe o KM INICIAL",@kmInicial)          
       MsgGet("Exercicio 4.2","Informe o KM FINAL",@kmFinal)          
       MsgGet("Exercicio 4.2","Informe o QUANTIDADE DE LITROS GASTOS",@qtdLtGasto)          
       MsgGet("Exercicio 4.2","Informe o PREÇO DO COMBUSTIVEL",@precoLtCombt)          
       MsgGet("Exercicio 4.2","Informe a CAPACIDADE DO TANQUE",@cptanque)

       MsgInfo(STR((kmFinal-kmInicial),10,2),"A quilometragem rodada foi:")          
       MsgInfo(STR(((kmFinal-kmInicial)/qtdLtGasto),10,2),"Km por Litro:")

       kmPorLitro:= (kmFinal-kmInicial)/qtdLtGasto
       atVeiculo :=  kmPorLitro*cptanque
       MsgInfo(STR((atVeiculo),10,2),"Autonomia do veículo:")

       custoViagem:= precoLtCombt*((kmFinal-kmInicial)/kmPorLitro)
       MsgInfo(STR((custoViagem),10,2),"Custo da viagem:")
       Return Nil

       
       
       
******* EXERCICIO 4.3 **********       
       Function Exercicio43 ()
********************************
       Local nHorasTrabalhadas:=0.00
       Local nValorHoraTrabalhada:=0.00
       Local nValorSalarioMinimo:=0.00
       Local nValorSalarioLiquido:=0.00
       Local nValorSalarioBruto:=0.00
       Local nValorImposto:=0.00
       
       MsgGet("Exercicio 4.3","Informe a quantide de horas trabalhadas",@nHorasTrabalhadas)
       MsgGet("Exercicio 4.3","Informe o Valor do Salario Minimo",@nValorSalarioMinimo)
       
       nValorHoraTrabalhada:= nValorSalarioMinimo*0.1
       nValorSalarioBruto:= nHorasTrabalhadas*nValorHoraTrabalhada
       nValorImposto:= nValorSalarioBruto*0.03
       nValorSalarioLiquido:= nValorSalarioBruto-nValorImposto
       
       
      /* ?nValorHoraTrabalhada
       ?nValorSalarioBruto
       ?nValorImposto
       ?nValorSalarioLiquido */
       
       MsgInfo(STR(nValorSalarioBruto),5.2,"O Valor do Salario Bruto é:")
       MsgInfo(STR(nValorImposto),5.2,"O Valor do Imposto é:")
       MsgInfo(STR(nValorSalarioLiquido),5.2,"O Valor do Salario Liquido é:")  
       
       
       Return Nil
