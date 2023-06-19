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

### Falha de Autenticação e Autorização

Suponha que um dispositivo de armazenamento USB criptografado seja protegido por uma senha para acessar os dados armazenados na memória não volátil. O dispositivo possui um mecanismo de autenticação embutido que solicita a senha ao usuário antes de desbloquear os dados.

No entanto, devido a uma falha de implementação ou projeto inadequado, o mecanismo de autenticação possui uma vulnerabilidade que permite a um invasor contornar a autenticação sem fornecer a senha correta. Essa falha pode ocorrer de várias maneiras, como:

Exploração de vulnerabilidades de software: O mecanismo de autenticação pode conter falhas de segurança no código ou na lógica que podem ser exploradas pelo invasor. Isso pode permitir que o invasor ignore o processo de autenticação e acesse diretamente os dados armazenados na memória não volátil.

Vazamento de informações confidenciais: Se houver um vazamento de informações confidenciais relacionadas à autenticação (como a senha ou a chave de criptografia) por meio de métodos como phishing, engenharia social ou exploração de outras vulnerabilidades no sistema, um invasor pode usar essas informações para acessar a memória não volátil sem a autenticação adequada.

Fraquezas na proteção física: Se o dispositivo de armazenamento não estiver adequadamente protegido fisicamente, um invasor pode obter acesso direto à memória não volátil sem passar pelo mecanismo de autenticação. Por exemplo, se o invasor conseguir abrir o dispositivo, retirar o chip de memória não volátil e conectá-lo a outro sistema, poderá acessar os dados diretamente, sem a necessidade de autenticação.

Em qualquer um desses casos, a falha de autenticação e autorização permite que um invasor acesse os dados armazenados na memória não volátil sem a devida autorização. Isso pode levar à exposição de informações confidenciais, como senhas, dados pessoais ou segredos comerciais, ou permitir que o invasor modifique ou exclua os dados armazenados.

É importante que os dispositivos de armazenamento que utilizam memória não volátil tenham robustas medidas de autenticação e autorização implementadas, além de serem submetidos a testes de segurança adequados para identificar e corrigir possíveis falhas de segurança nessa área.

### Injeção de Firmware

Suponha que um dispositivo eletrônico, como um roteador Wi-Fi, utilize um chip de memória não volátil para armazenar o firmware responsável por controlar suas funcionalidades e operações. O firmware é o software de baixo nível que executa as instruções necessárias para o funcionamento do dispositivo.

Um invasor mal-intencionado consegue explorar uma vulnerabilidade no sistema operacional do dispositivo ou em seu processo de atualização de firmware. Essa vulnerabilidade permite que o invasor injete um firmware modificado ou malicioso na memória não volátil do dispositivo, substituindo o firmware original.

Ao fazer isso, o invasor pode inserir código malicioso no firmware que permite o controle remoto do dispositivo ou a execução de ações indesejadas. Por exemplo:

Backdoors: O invasor pode inserir um backdoor no firmware, que é uma porta de entrada secreta para acessar o dispositivo de forma não autorizada. Isso permite que o invasor tenha controle total sobre o dispositivo, podendo realizar atividades como espionagem, monitoramento de tráfego de rede ou execução de comandos arbitrários.

Modificação de configurações: O invasor pode alterar as configurações do dispositivo no firmware, como alterar senhas, redirecionar o tráfego da rede ou desativar medidas de segurança existentes. Isso pode comprometer a integridade e a segurança das operações do dispositivo.

Expansão de funcionalidades maliciosas: O invasor pode adicionar funcionalidades maliciosas ao firmware que podem causar danos ao dispositivo ou à rede em que está conectado. Por exemplo, ele pode implementar um mecanismo de distribuição de malware para infectar outros dispositivos na rede.

A injeção de firmware é uma forma sofisticada de ataque que requer conhecimento técnico avançado e acesso ao dispositivo ou aos sistemas que controlam a memória não volátil. Para mitigar essa ameaça, é importante seguir as práticas recomendadas de segurança, como aplicar atualizações de firmware regularmente, utilizar assinaturas digitais para verificar a autenticidade do firmware e implementar medidas de segurança adicionais, como criptografia e controle de acesso aos mecanismos de atualização de firmware.

### Acesso não autorizado
Suponha que um usuário tenha um dispositivo de armazenamento USB que utiliza memória não volátil para armazenar seus arquivos pessoais. Esse dispositivo está protegido por uma senha para evitar acesso não autorizado.

Um invasor mal-intencionado obtém acesso físico ao dispositivo USB enquanto o usuário está ausente e deseja acessar os arquivos armazenados nele. O invasor tenta várias abordagens para contornar a senha de proteção.

Primeiro, o invasor tenta força bruta, onde ele utiliza um programa automatizado para tentar várias combinações de senhas até encontrar a correta. Se a senha escolhida pelo usuário for fraca ou previsível, o invasor pode ter sucesso nessa tentativa.

Outra abordagem que o invasor pode tentar é a exploração de uma vulnerabilidade no sistema operacional que lida com a proteção de senhas ou criptografia da memória não volátil. Se o sistema operacional tiver uma falha de segurança conhecida, o invasor pode explorá-la para contornar as medidas de proteção e acessar os dados armazenados na memória não volátil.

Além disso, o invasor também pode tentar utilizar técnicas de engenharia social para obter informações da senha do usuário. Isso pode ser feito através de phishing, onde o invasor envia mensagens falsas ou cria páginas de login falsas para enganar o usuário e obter sua senha.

Se o invasor conseguir contornar a proteção e acessar a memória não volátil do dispositivo, ele pode ler, copiar, modificar ou excluir os arquivos pessoais do usuário sem sua autorização.








REFERENCIAS =

https://learn.microsoft.com/en-us/windows/security/information-protection/tpm/trusted-platform-module-overview
