#  Processamento de Dados Genômicos e Inferências Filogenéticas de Sequênciamento de Nova Geração
O presente repositório foi criado com o intuito de facilitar o processamento de dados genômicos obtidos por meio de sequenciamento de nova geração, gerados por biblioteca de target-enrichment sequencing com o painel Cactaceae591 (Romeiro-Brito et al. 2022) e a construção de inferências filogenéticas, incluindo a trimagem de dados, montagem de locos, análise de qualidade e construção de árvores gene e espécies. Os programas e comandos necessários devem ser executados no sistema operacional Linux (ou no Subsistema Linux para Windows), através da interface Bash.

##  Índice
1.  [Comandos básicos do Linux](#Comandos-básicos-do-Linux)
2.  [Filtragem inicial dos dados brutos](#Filtragem-inicial-dos-dados-brutos)
3.  [Montagem dos loci](#Montagem-dos-loci)
4.  [Identificação e remoção de loci parálogos](#Identificação-e-remoção-de-loci-parálogos)
5.  [Polimento das sequências homologas](#Polimento-das-sequências-homologas)
6.  [Remoção de regiões hipervariáveis (spruceup)](#Remoção-de-regiões-hipervariáveis-(spruceup))
7.  [Inferência filogenética concatenada - Máxima Verossimilhança](#Inferência-filogenética-concatenada--Máxima-Verossimilhança)
8.  [Inferência filogenética com o método de coalescência](#Inferência-filogenética-com-o-método-de-coalescência)

##  Comandos básicos do Linux
```
**criar lista** → ls *.fastq > namelist.txt
**entrar na pasta** → cd nome_pasta/pasta_seguinte
**sair de uma pasta** → cd ../
**sair de duas pastas** → cd ../..
**criar pasta** → mkdir nome_pasta
**para ver a última linha do arquivo** -> tail nome_arquivo
**para ver o arquivo completo** → less
**criar ou editar um arquivo** → nano nome_arquivo.txt
**contagem de arquivos** → ls -1 | wc -l
**ver o diretório que está** → pwd
**limpar terminal** → clear
**para ver dados usados pelo computador** → htop
**mover arquivo** → mv arquivo ./nome_pasta
**copiar arquivo** → cp arquivo ./nome_pasta
```
## Filtragem inicial dos dados brutos
**Objetivo**: Remover sequencias de baixa qualidade e os adaptadores para garantir uma análise mais precisa dos dados






