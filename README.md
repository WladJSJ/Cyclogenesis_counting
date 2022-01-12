# Cyclogenesis_counting

Este script faz a detecção de ciclogênese (formação de um ciclone) observada nas reanálises do CFSR (pode ser facilmente adaptado para qq outra reanálise).

A detecção pode ser feita por dois critérios:
1) Vorticidade relativa em 825hPa (mais usual):
   O programa compara cada ponto de grade com seus vizinhos, identificando um ponto de mínima vorticidade relativa.
   Se a vorticidade nesse ponto for menor que um limiar estabelecido, este será considerado um ciclone.
2) Pressão em superfície reduzida ao nível médio do mar:
   Nesse caso, uma vez identificado um ponto de pressão mínima, se a concavidade do campo de pressão 
   ultrapassar um limiar estabelecido, este ponto será considerado como um ciclone.
   
Ambos os critérios podem ser utilizados concomitantemente, e o ponto de detecção será o ponto médio dado por ambos os métodos.

Os arquivos de entrada (netcdf) estão numa grade regular de 2.5x2.5 graus. São arquivos mensais, com time-step de 6h. Outros tipo de arquivo e/ou estrutura dos
dados podem ser utilizadas, fazendo-se as adaptações necessárias.

A estrutura do nome do arquivo é prmsl.l.gdas.{ANO}{MES}.grb2.nc
Exemplo:
prmsl.l.gdas.198001.grb2.nc

Divirtam-se
