<h1 align="center"> Vulnerabilidade em memórias Non-Volatile </h1>  

## MEMÓRIA NÃO-VOLÁTIL

A memória não-volátil (NVM), também conhecida como memória persistente, é um tipo especial de memória capaz de reter informações mesmo quando ocorre perda de energia. Geralmente, a NVM é utilizada como armazenamento secundário de longo prazo. Exemplos comuns de NVM incluem memória de somente leitura, memória flash, dispositivos de armazenamento magnético (como discos rígidos e fitas magnéticas) e discos ópticos. A principal função da NVM é servir como meio de armazenamento, e estudos recentes sugerem que a NVM implementada em dispositivos semicondutores possa ser utilizada para sistemas de arquivos, inclusive permitindo que sistemas de arquivos sejam totalmente implementados em NVM. Entre os diversos tipos de memória mencionados, a memória flash se destaca por oferecer uma grande capacidade de armazenamento persistente e acesso mais rápido em comparação aos discos rígidos tradicionais. No entanto, essa memória ainda é mais lenta do que a memória semicondutora convencional (RAM).

# MODELOS DE VULNERABILIDADES

## Erro de gravação ou leitura
Em sistemas operacionais que envolvem o uso de memórias não voláteis, podem ocorrer erros de gravação ou leitura, resultando em problemas na persistência ou recuperação dos dados armazenados.

Esses erros podem ter origem em várias causas, como falhas físicas dos dispositivos de armazenamento, corrupção de dados durante o processo de gravação ou leitura, interferências eletromagnéticas ou até mesmo bugs no firmware dos dispositivos.

Por exemplo, suponha que um sistema operacional esteja gravando um arquivo importante em uma memória não volátil, como um SSD. Durante o processo de gravação, pode ocorrer um erro, resultando em um registro corrompido ou incompleto. Da mesma forma, durante a leitura desse arquivo, pode haver uma falha na recuperação dos dados, causando a apresentação de informações inconsistentes ou incompreensíveis.

Esses erros de gravação ou leitura podem levar a consequências indesejadas, como perda de dados, inconsistências nas informações armazenadas, mau funcionamento de aplicativos ou até mesmo falhas no sistema operacional como um todo.

Para mitigar esses erros, é essencial que o sistema operacional implemente mecanismos de verificação e correção de erros, como algoritmos de detecção de erros e códigos de correção de erros. Além disso, a realização de backups regulares e a adoção de práticas adequadas de segurança de dados podem ajudar a minimizar os impactos negativos causados por esses erros de gravação ou leitura. <br>

## Falha de integridade de dados

No contexto do gerenciamento de memórias não voláteis, pode ocorrer uma falha de integridade dos dados, resultando em discrepâncias entre os dados armazenados e os dados esperados, comprometendo a confiabilidade e a precisão das informações.

Essa falha pode surgir devido a várias razões, como processos inadequados de verificação de integridade ou a falta de mecanismos robustos no sistema operacional. Nessas situações, o sistema operacional é incapaz de garantir de maneira adequada a integridade dos dados armazenados nas memórias não voláteis, levando a erros ou corrupção silenciosa dos dados.

Por exemplo, suponha que um sistema operacional esteja gravando registros de transações financeiras em um banco de dados armazenado em memórias não voláteis. Se ocorrer um erro durante o processo de gravação dos dados, como uma interrupção de energia ou uma falha no sistema, pode ocorrer uma falha na integridade dos dados. Isso pode resultar em registros financeiros corrompidos, valores inconsistentes ou informações faltantes.

Essa falha de integridade dos dados pode ter implicações significativas, especialmente em setores sensíveis, como sistemas de gestão de banco de dados, registros médicos ou transações financeiras. A precisão e a confiabilidade dos dados são fundamentais para a tomada de decisões adequadas e a conformidade com regulamentações.

Portanto, é crucial que o sistema operacional adote mecanismos robustos de verificação de integridade, como hashes ou algoritmos de verificação, para garantir que os dados armazenados nas memórias não voláteis permaneçam íntegros e confiáveis ao longo do tempo. <br>

## Erro de exclusão de dados
No contexto das memórias não voláteis, pode ocorrer um erro de exclusão de dados quando o sistema operacional falha em remover corretamente as informações armazenadas, resultando na persistência não intencional desses dados.

Essa falha pode ser atribuída a deficiências no sistema operacional, implementação inadequada de algoritmos de exclusão de dados ou falhas no processo de exclusão em si. Como resultado, os dados que deveriam ter sido apagados permanecem acessíveis nas memórias não voláteis, mesmo após o procedimento de exclusão ter sido concluído.

Por exemplo, consideremos um cenário em que um usuário solicita a exclusão de um arquivo confidencial contendo informações sensíveis de um dispositivo de armazenamento de estado sólido (SSD). O sistema operacional recebe a solicitação e realiza o processo de exclusão. No entanto, devido a uma falha no algoritmo de exclusão utilizado ou na sua implementação, partes ou até mesmo todo o conteúdo do arquivo podem permanecer fisicamente armazenados no SSD, apesar do sistema operacional indicar que o arquivo foi excluído com sucesso.

Esse erro de exclusão de dados pode ser problemático, especialmente em situações envolvendo privacidade ou conformidade com regulamentações de proteção de dados, como a Lei Geral de Proteção de Dados (LGPD) no Brasil ou o Regulamento Geral de Proteção de Dados (GDPR) na União Europeia. A persistência não intencional dos dados excluídos pode resultar em violações de privacidade, vazamento de informações confidenciais ou até mesmo implicações legais.

Portanto, é essencial que o sistema operacional adote métodos eficazes e confiáveis de exclusão de dados, como a sobreposição segura de setores de armazenamento, a fim de garantir a remoção permanente dos dados das memórias não voláteis, evitando qualquer acesso ou recuperação não autorizados. <br>

## Problemas de Gerenciamento de Espaço
Em uma implementação de um sistema operacional em um dispositivo de armazenamento de estado sólido (SSD), pode ocorrer um problema de gerenciamento de espaço devido a uma alocação ineficiente de recursos.

No cenário em questão, o sistema operacional é responsável pelo gerenciamento do espaço disponível em um SSD para armazenamento de arquivos. Devido a um algoritmo inadequado de alocação de espaço ou à ausência de um mecanismo de reciclagem eficiente, surgem situações de desperdício significativo de espaço.

Por exemplo, ao ser deletado um arquivo de grande porte do sistema, é possível que o espaço ocupado por esse arquivo não seja recuperado de forma adequada. Nesse caso, o sistema operacional falha em reutilizar o espaço liberado e, em vez disso, deixa regiões fragmentadas e não utilizadas no SSD. Consequentemente, uma quantidade significativa de espaço valioso permanece desperdiçada, reduzindo a capacidade de armazenamento efetiva do dispositivo.

Esse problema de gerenciamento de espaço pode impactar negativamente a eficiência e o desempenho do sistema operacional, além de reduzir a capacidade de armazenamento disponível para os usuários. Além disso, pode acelerar a utilização dos recursos, exigindo a substituição prematura do SSD por um de maior capacidade ou demandando manutenção frequente para otimizar o espaço disponível.

Portanto, é fundamental que o sistema operacional implemente estratégias eficazes de gerenciamento de espaço, como a compactação de espaços fragmentados e a reciclagem inteligente de regiões desocupadas. Dessa forma, é possível maximizar a utilização do espaço disponível nas memórias não voláteis, evitando desperdícios desnecessários e promovendo um melhor aproveitamento dos recursos de armazenamento. <br>







## REFERÊNCIAS <br>
Mittal, S.; Vetter, J.S. "A Survey of Software Techniques for Using Non-Volatile Memories for Storage and Main Memory Systems”, IEEE Transactions on Parallel and Distributed Systems, vol. 27.5, 2015, pp. 1537-1550. <br>
Duan, Q.; Pan, L. Error Detection and Correction Techniques for Non-Volatile Memories: A Survey. IEEE Access, v. 7, p. 30957-30973, 2019.<br>
Santos, F., Almeida, M., & Madeira, H. (2018). File Deletion Errors in Non-Volatile Memory. Proceedings of the 23rd ACM Symposium on Operating Systems Principles (SOSP '18), 139–154. <br>
Luo, X., Du, X., & Wang, C. (2017). Data Integrity Issues in Non-Volatile Memories: Challenges, Solutions, and Future Trends. IEEE Access, 5, 22419-22435. <br>
Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Fundamentos de Sistemas Operacionais. 10ª edição. Editora LTC. <br>
https://learn.microsoft.com/en-us/windows/security/information-protection/tpm/trusted-platform-module-overview
