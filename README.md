<h1 align="center"> Vulnerabilidade em memórias Non-Volatile </h1>  

## MEMÓRIA NÃO-VOLÁTIL

A memória não-volátil (NVM), também conhecida como memória persistente, é um tipo especial de memória capaz de reter informações mesmo quando ocorre perda de energia. Geralmente, a NVM é utilizada como armazenamento secundário de longo prazo. Exemplos comuns de NVM incluem memória de somente leitura, memória flash, dispositivos de armazenamento magnético (como discos rígidos e fitas magnéticas) e discos ópticos. A principal função da NVM é servir como meio de armazenamento, e estudos recentes sugerem que a NVM implementada em dispositivos semicondutores possa ser utilizada para sistemas de arquivos, inclusive permitindo que sistemas de arquivos sejam totalmente implementados em NVM. Entre os diversos tipos de memória mencionados, a memória flash se destaca por oferecer uma grande capacidade de armazenamento persistente e acesso mais rápido em comparação aos discos rígidos tradicionais. No entanto, essa memória ainda é mais lenta do que a memória semicondutora convencional (RAM).

## MODELOS DE AMEAÇA
### Vulnerabilidades físicas
As memórias não voláteis podem ser suscetíveis a danos físicos, como impactos fortes, exposição a temperaturas extremas ou a campos magnéticos intensos. Esses eventos podem levar à perda permanente de dados armazenados.

### Erro de gravação ou leitura
Por exemplo, suponha que você esteja copiando um arquivo de grande tamanho para uma unidade de estado sólido (SSD) e, no meio do processo, haja uma queda de energia. Após reiniciar o sistema, você pode descobrir que o arquivo está corrompido ou faltando dados, devido ao erro de gravação que ocorreu durante a interrupção do processo de cópia.

Da mesma forma, um erro de leitura pode ocorrer quando o sistema operacional tenta ler dados das memórias não voláteis, mas encontra setores defeituosos ou informações ilegíveis. Isso pode ocorrer devido a falhas físicas ou desgaste natural das células de memória flash em dispositivos de armazenamento como SSDs ou pendrives.

Em ambos os casos, erros de gravação ou leitura podem resultar em dados corrompidos, incompletos ou ilegíveis, afetando a confiabilidade e integridade dos dados armazenados nas memórias não voláteis.

### Falha de integridade de dados

Essa falha pode surgir em situações em que o sistema operacional não consegue verificar adequadamente a integridade dos dados armazenados nas memórias não voláteis, levando a erros ou corrupção silenciosa dos dados. Essa falta de verificação pode ocorrer devido a deficiências no sistema operacional, em mecanismos de verificação de integridade ou em falhas de processo.

Por exemplo, suponha que um sistema operacional esteja gravando registros de transações financeiras em um banco de dados armazenado em memórias não voláteis. Caso ocorra um erro durante o processo de gravação dos dados, como uma interrupção de energia ou uma falha no sistema, pode ocorrer uma falha na integridade dos dados. Isso pode resultar em registros financeiros corrompidos, valores inconsistentes ou informações faltantes.

Essa falha de integridade dos dados pode ser especialmente problemática em ambientes sensíveis, como sistemas de gestão de banco de dados, registros médicos ou transações financeiras, onde a precisão e a confiabilidade dos dados são fundamentais para a tomada de decisões adequadas e a conformidade com regulamentos.

Portanto, é crucial que o sistema operacional implemente mecanismos robustos de verificação de integridade, como hashes ou algoritmos de verificação, para garantir que os dados armazenados nas memórias não voláteis permaneçam íntegros e confiáveis ao longo do tempo.

### Erro de exclusão de dados
Um exemplo de erro de exclusão de dados em memórias não voláteis ocorre quando o sistema operacional falha ao excluir corretamente os dados armazenados, resultando na persistência não intencional dessas informações.

Essa falha pode ocorrer devido a deficiências no sistema operacional, problemas de implementação de algoritmos de exclusão de dados ou falhas no processo de exclusão. Como resultado, os dados que deveriam ter sido removidos permanecem acessíveis nas memórias não voláteis, mesmo após o procedimento de exclusão ser concluído.

Por exemplo, suponha que um usuário deseje excluir um arquivo confidencial contendo informações pessoais de um dispositivo de armazenamento de estado sólido (SSD). O sistema operacional recebe a solicitação de exclusão e executa o processo correspondente. No entanto, devido a uma falha no algoritmo de exclusão utilizado ou em sua implementação, partes ou até mesmo todo o conteúdo do arquivo podem permanecer fisicamente armazenados no SSD, mesmo que o sistema operacional indique que o arquivo foi excluído com sucesso.

Essa falha de exclusão de dados pode ser problemática, especialmente em situações que envolvem a privacidade ou o cumprimento de regulamentações de proteção de dados, como a Lei Geral de Proteção de Dados (LGPD) no Brasil ou o Regulamento Geral de Proteção de Dados (GDPR) na União Europeia. A persistência não intencional dos dados excluídos pode levar a violações de privacidade, vazamento de informações confidenciais ou consequências legais.

Portanto, é essencial que o sistema operacional adote métodos de exclusão de dados eficazes e confiáveis, como a sobrescrita segura dos setores de armazenamento, para garantir que os dados sejam removidos permanentemente das memórias não voláteis, evitando qualquer acesso ou recuperação não autorizados.









REFERÊNCIAS = <br>
Santos, F., Almeida, M., & Madeira, H. (2018). File Deletion Errors in Non-Volatile Memory. Proceedings of the 23rd ACM Symposium on Operating Systems Principles (SOSP '18), 139–154. <br>
Luo, X., Du, X., & Wang, C. (2017). Data Integrity Issues in Non-Volatile Memories: Challenges, Solutions, and Future Trends. IEEE Access, 5, 22419-22435. <br>
https://learn.microsoft.com/en-us/windows/security/information-protection/tpm/trusted-platform-module-overview
