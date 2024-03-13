
# Start up sequence and BIOS

![[Pasted image 20240301184616.png]]

- Sector (uma divisão física do disco, assim como um livro está dividido em páginas sequencialmente ordenadas)
- Boot sector (tem o código necessário para arrancar o sistema operativo, é o primeiro setor numa drive) tem o mapa da divisão lógica do disco.

- ![[Pasted image 20240301185820.png]]

# Malware software malicioso
- o virus é um tipo de malware que se multiplica
![[Pasted image 20240301192158.png]]

Se o malware estiver no bootsector, está alojado num sitio que roda antes do sistema operativo e não se consegue identificar com os antivirus
Startup sequence ( coisas que acontecem em determinada sequencia com um porquê)
 
![[Pasted image 20240301194426.png]]

MBR é a tabela de partições do disco (GPT é uma tecnologia mais recente)
![[Pasted image 20240301195911.png]]
![[Pasted image 20240301200032.png]]
![[Pasted image 20240301202914.png]]
O UEFI é um software e fica num chip dedicado ou numa partição do disco, pode ser atualizado, secure boot (tem que desativar para instalar o sistema operativo)

![[Pasted image 20240301204534.png]]
![[Pasted image 20240301204642.png]]
 Lab de hoje:
 slack 04