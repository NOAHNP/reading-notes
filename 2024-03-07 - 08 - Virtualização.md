
![[Pasted image 20240307185347.png]]
queremos o lab para virtualizar e vamos aceder ao LAB remotamente.  RDM team viewer pelo port 3389

Virtualização: é um processo de criação de maquinas virtuais, criar uma maquina dentro de outra maquina, pode não ser ao nível do sistema operativo. é uma representação virtual de componentes físicos.
dependo de recursos físicos da maquina, CPU, RAM.... para rodar a virtualização.
a instancia gere o processamento virtual, a capacidade distribuida

![[Pasted image 20240307192018.png]]

O hypervisor é responsável pela gestão de recursos, criação e eliminação, isolamento, para maquinas virtuais

type 1 - é instalado diretamente no hardware para evitar consumos de recursos desnecessários pelo sistema operacional

type 2 - é instalado em cima de um sistema operativo

![[Pasted image 20240307192937.png]]

para virtualizar uma coisa pequenina como uma app, que não precisa de um sistema operativo inteiro com todos os recurso, se eu quiser virtualizar só uma app podemos usas o docker

O Docker é um projeto opensource que faz um processo de containerização. Ateção o docker não é um hypervisor pesar da ideia ser igual ao de uma virtualização.
abstrai tudo a baixo da app. enquanto o virtualbox por exemplo abstrai tudo a baixo do sistema operacional.

os containers partilha o kernel do sistema operativo onde as apps estão a rodar. 


![[Pasted image 20240307200126.png]]
![[Pasted image 20240307200137.png]]
A diferença entre virtualização e containerização.

![[Pasted image 20240307201048.png]]

![[Pasted image 20240307201343.png]]
![[Pasted image 20240307201605.png]]

![[Pasted image 20240307202030.png]]

![[Pasted image 20240307202723.png]]

![[Pasted image 20240307204435.png]]
![[Pasted image 20240307204951.png]]

![[Pasted image 20240307205049.png]]

![[Pasted image 20240307205558.png]]
![[Pasted image 20240307205659.png]]
- dar o nome que quiser - rodolfo chamou winsoes 10 dummy
- folder é onde vai ficar armazenado todos os ficheiros que tem a ver com esta maquina
- em iso imagem, CF, é o CD ou DVD onde vamos buscar o sistema operativo para ser instalado
![[Pasted image 20240307205908.png]]
aqui posso colocar o que eu quisere apagar os cardinais da licensa
![[Pasted image 20240307205923.png]]
aconselha colocar 4 de memoria ram e 2 Core(CPU)
![[Pasted image 20240307210105.png]]
não escolher pre allocate full size, vou reservar só 50GB que vão sento progressivamente utilizados. se eu fizer o pre allocate full size ele realoca logo os 50GB para esta maquina

nex vem a revisão
![[Pasted image 20240307210243.png]]

![[Pasted image 20240307210318.png]]
agora é como instalar um OS qualquer.

![[Pasted image 20240307210530.png]]
![[Pasted image 20240307210539.png]]
estes são os settings e da para mudar configurações como
![[Pasted image 20240307210622.png]]

![[Pasted image 20240307210633.png]]

utilizar o NAT que é para ter acesso a net

![[Pasted image 20240307210715.png]]
da para remover ou não cabos de rede


Há várias razões pelas quais você pode querer criar máquinas virtuais:

1. **Testes e Desenvolvimento:** Máquinas virtuais oferecem um ambiente seguro para testar novos softwares, configurações de rede, ou mesmo sistemas operacionais, sem comprometer o seu sistema principal.
    
2. **Isolamento:** Ao criar máquinas virtuais, você pode isolar diferentes serviços ou aplicativos para evitar interferências entre eles. Isso é especialmente útil para desenvolvedores que precisam de ambientes isolados para diferentes projetos.
    
3. **Conservação de Recursos:** Usar máquinas virtuais pode ajudar a economizar recursos de hardware, pois várias máquinas podem ser executadas em um único servidor físico, otimizando o uso de CPU, memória e armazenamento.
    
4. **Segurança:** Máquinas virtuais podem ser usadas para executar softwares potencialmente perigosos ou suspeitos em um ambiente isolado, protegendo assim o seu sistema principal de possíveis ameaças.
    
5. **Backup e Recuperação:** Máquinas virtuais podem ser facilmente clonadas e copiadas, o que facilita a criação de backups e recuperação rápida em caso de falhas ou perda de dados.
    
6. **Desenvolvimento de Software Multiplataforma:** Desenvolvedores podem usar máquinas virtuais para testar seus aplicativos em diferentes sistemas operacionais sem a necessidade de hardware adicional.
    

Em resumo, as máquinas virtuais oferecem flexibilidade, segurança e eficiência, sendo uma ferramenta valiosa para uma variedade de propósitos, desde desenvolvimento de software até segurança cibernética e gerenciamento de recursos de TI.

As máquinas virtuais oferecem um ambiente seguro principalmente devido ao isolamento que proporcionam. Aqui estão algumas maneiras pelas quais as máquinas virtuais garantem esse ambiente:

1. **Isolamento de Recursos:** Cada máquina virtual é executada em um ambiente virtualizado separado, com recursos de hardware alocados de forma independente. Isso impede que as máquinas virtuais interfiram umas com as outras em termos de processamento, memória e armazenamento.
    
2. **Sandboxing:** As máquinas virtuais criam um "sandbox" onde você pode executar aplicativos ou realizar tarefas sem que elas tenham acesso direto ao sistema operacional host ou a outros aplicativos em execução. Isso ajuda a prevenir que malware ou softwares mal-intencionados causem danos ao sistema principal.
    
3. **Snapshot e Rollback:** Muitas plataformas de virtualização permitem que você tire "snapshots" das máquinas virtuais em determinados pontos no tempo. Isso permite que você reverta facilmente para um estado anterior da máquina virtual se algo der errado, como uma infecção por malware.
    
4. **Rede Separada:** As máquinas virtuais podem ser configuradas com redes virtuais isoladas, o que impede que elas acessem a rede física ou se comuniquem diretamente com outras máquinas fora do ambiente virtual.
    
5. **Clonagem e Descarte:** Você pode facilmente clonar uma máquina virtual para criar cópias idênticas para testes ou desenvolvimento. Se uma máquina virtual for comprometida, você pode simplesmente descartá-la e criar uma nova cópia a partir de um snapshot anteriormente salvo.
    

Esses recursos combinados oferecem um ambiente seguro onde você pode testar aplicativos, executar software suspeito e realizar outras atividades sem comprometer a segurança do sistema operacional principal ou de outros aplicativos em execução.

Embora as máquinas virtuais forneçam um alto nível de segurança e isolamento, não há garantia de que elas sejam completamente seguras. Existem algumas maneiras pelas quais a segurança de uma máquina virtual pode ser violada:

1. **Vulnerabilidades na Virtualização:** Assim como qualquer software, as plataformas de virtualização podem conter vulnerabilidades que podem ser exploradas por invasores para comprometer as máquinas virtuais ou o hipervisor.
    
2. **Ataques de Fuga (Escape):** Em casos raros, os ataques de fuga (escape) permitem que um invasor escape do ambiente da máquina virtual e acesse o sistema operacional host ou outras máquinas virtuais no mesmo servidor físico.
    
3. **Ataques de Rede:** Se as configurações de rede das máquinas virtuais não forem adequadamente protegidas, um invasor pode explorar vulnerabilidades na rede para comprometer a segurança das máquinas virtuais ou dos sistemas conectados a elas.
    
4. **Malware Específico para Virtualização:** Alguns tipos de malware são projetados especificamente para atacar ambientes de virtualização, explorando vulnerabilidades ou usando técnicas avançadas para comprometer a segurança das máquinas virtuais.
    
5. **Ataques de Engenharia Social:** Ataques de engenharia social, como phishing, podem ser usados para obter acesso aos sistemas hospedeiros ou às credenciais de acesso às máquinas virtuais.
    

Embora esses riscos existam, é importante ressaltar que, quando configuradas e gerenciadas corretamente, as máquinas virtuais ainda oferecem um alto nível de segurança e são amplamente utilizadas em ambientes corporativos e de desenvolvimento. A implementação de práticas de segurança sólidas, como atualizações regulares, configurações de rede seguras e monitoramento proativo, pode ajudar a mitigar muitos desses riscos.

Existem várias razões pelas quais você pode preferir usar Docker e criar contêineres em vez de criar máquinas virtuais:

1. **Eficiência de Recursos:** Os contêineres compartilham o kernel do sistema operacional do host, o que significa que são mais leves em comparação com as máquinas virtuais, que exigem seu próprio sistema operacional completo. Isso resulta em uma utilização mais eficiente dos recursos do sistema, permitindo que você execute mais contêineres em um único host.
    
2. **Inicialização Rápida:** Os contêineres são inicializados rapidamente, em questão de segundos, enquanto as máquinas virtuais podem levar vários minutos para serem iniciadas. Isso é especialmente útil em ambientes de desenvolvimento e implantação, onde você precisa escalar rapidamente ou provisionar novos serviços.
    
3. **Portabilidade:** Os contêineres são independentes da infraestrutura subjacente, o que significa que você pode movê-los facilmente entre diferentes ambientes, como máquinas físicas, máquinas virtuais ou na nuvem, sem precisar modificar o aplicativo ou suas dependências.
    
4. **Gerenciamento Simplificado:** Docker fornece ferramentas poderosas para criar, implantar e gerenciar contêineres de forma eficiente. Com Docker Compose e Kubernetes, você pode facilmente orquestrar e escalar contêineres em clusters de qualquer tamanho.
    
5. **Isolamento Leve:** Embora os contêineres forneçam isolamento entre aplicativos e suas dependências, eles ainda compartilham o mesmo kernel do sistema operacional do host. Isso pode ser vantajoso em termos de desempenho e eficiência de recursos, desde que você confie na segurança do ambiente do host.
    
6. **Padrão da Indústria:** Docker e contêineres tornaram-se um padrão da indústria para o desenvolvimento e implantação de aplicativos, com um amplo ecossistema de ferramentas e suporte da comunidade.
    

Em resumo, usar Docker e contêineres oferece eficiência, portabilidade, gerenciamento simplificado e rapidez de inicialização em comparação com a criação de máquinas virtuais, tornando-os uma escolha atraente para uma variedade de cenários de desenvolvimento e implantação.

  
Embora os contêineres ofereçam um nível de isolamento entre os aplicativos e suas dependências, é possível violar esse isolamento em certas circunstâncias. Aqui estão alguns cenários em que o isolamento de contêineres pode ser comprometido:

1. **Vulnerabilidades no Kernel:** Como os contêineres compartilham o kernel do sistema operacional do host, vulnerabilidades no kernel podem ser exploradas por invasores para acessar outros contêineres ou o sistema operacional host.
    
2. **Escalada de Privilégios:** Em alguns casos, um invasor pode explorar uma vulnerabilidade dentro do próprio contêiner para obter acesso privilegiado ao sistema operacional host.
    
3. **Vazamento de Informações:** Se não configurados corretamente, contêineres podem vazar informações sensíveis através de canais laterais, como compartilhamento de recursos de rede ou memória.
    
4. **Ataques de Rede:** Contêineres conectados à mesma rede podem ser alvos de ataques de rede internos, como ataques de negação de serviço (DDoS) ou ataques de spoofing.
    
5. **Falhas na Configuração de Segurança:** Configurações inadequadas de segurança, como permissões excessivas ou compartilhamento inadequado de volumes, podem comprometer o isolamento entre contêineres.
    
6. **Imagens de Contêiner Comprometidas:** Usar imagens de contêiner de fontes não confiáveis ou não verificar a integridade das imagens pode resultar na execução de contêineres com software malicioso embutido.
    

Embora esses riscos existam, é importante ressaltar que a maioria das implementações de contêineres oferece um bom nível de isolamento por padrão e muitas dessas vulnerabilidades podem ser mitigadas com práticas de segurança adequadas, como atualizações regulares, monitoramento de segurança e implementação de políticas de acesso e controle. Além disso, tecnologias emergentes, como os mecanismos de sandboxing e as soluções de segurança específicas para contêineres, estão sendo desenvolvidas para fortalecer ainda mais o isolamento de contêineres.