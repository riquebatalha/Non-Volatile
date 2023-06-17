<h1 align="center"> Vulnerabilidade em memórias Non-Volatile </h1>  

## MEMÓRIA NÃO-VOLÁTIL

A memória não-volátil (NVM), também conhecida como memória persistente, é um tipo especial de memória capaz de reter informações mesmo quando ocorre perda de energia. Geralmente, a NVM é utilizada como armazenamento secundário de longo prazo. Exemplos comuns de NVM incluem memória de somente leitura, memória flash, dispositivos de armazenamento magnético (como discos rígidos e fitas magnéticas) e discos ópticos. A principal função da NVM é servir como meio de armazenamento, e estudos recentes sugerem que a NVM implementada em dispositivos semicondutores possa ser utilizada para sistemas de arquivos, inclusive permitindo que sistemas de arquivos sejam totalmente implementados em NVM. Entre os diversos tipos de memória mencionados, a memória flash se destaca por oferecer uma grande capacidade de armazenamento persistente e acesso mais rápido em comparação aos discos rígidos tradicionais. No entanto, essa memória ainda é mais lenta do que a memória semicondutora convencional (RAM).

## MODELOS DE AMEAÇA

### Falhas na autenticação e autorização
### TPM - Trusted Platform Module
O TPM é um chip de segurança integrado em computadores e dispositivos eletrônicos. Ele fornece funções relacionadas à segurança baseadas em hardware, projetadas para proteger informações confidenciais, realizar operações criptográficas e garantir a integridade da plataforma.

O TPM é um criptoprocessador seguro que inclui múltiplos mecanismos de segurança física para torná-lo resistente a violações. Ele é responsável por gerar, armazenar e limitar o uso de chaves criptográficas, que são essenciais para proteger dados sensíveis e autenticar dispositivos.

Além disso, o TPM registra medidas de segurança do processo de inicialização, verificando a integridade do código de inicialização, firmware e componentes do sistema operacional. Essas medidas são usadas para garantir que o sistema tenha sido iniciado corretamente e para evitar que softwares maliciosos ou alterações não autorizadas comprometam a segurança da plataforma.

O TPM também pode ser utilizado para realizar operações criptográficas, como a criptografia e descriptografia de dados, assinatura digital e autenticação. Ele oferece uma camada adicional de segurança, pois as chaves e operações criptográficas são realizadas dentro do chip TPM, protegendo-as contra ataques externos.

Quando o TPM é utilizado para autenticação, ele pode ajudar a prevenir acesso não autorizado à memória não volátil, garantindo que apenas usuários ou dispositivos confiáveis tenham acesso aos dados armazenados. Além disso, o TPM também pode fornecer chaves de autenticação para verificar a identidade de um sistema ou aplicativo antes de permitir o acesso à memória não volátil.

Se houver falhas de segurança no processo de autenticação ou autorização implementado pelo TPM, isso pode abrir brechas para que um invasor acesse indevidamente a memória não volátil ou realize ações não autorizadas, como modificar ou excluir dados.









REFERENCIAS =

https://learn.microsoft.com/en-us/windows/security/information-protection/tpm/trusted-platform-module-overview
