# IngressoJa
Estrutura de um site para venda de ingressos, o objetivo dessa arquitetura é criar um sistema de vendas de ingressos eficiente e justo para um evento de grande concorrência, como um mega show de Rock em Rio. Ela visa atender a várias necessidades e desafios, essa arquitetura tem como objetivo criar uma experiência de compra de ingressos justa e eficiente para os clientes, onde todos tenham a oportunidade de adquirir ingressos para o evento desejado. Ela combina elementos técnicos, como rate limiting, filas de espera e balanceamento de carga, com políticas e procedimentos para garantir uma operação tranquila e segura durante a venda de ingressos. Amigávelmente nomeada de <b>INGRESSOJÁ</b>

<h1>Front-end do Site:</h1>

Página de Login: Os clientes devem fazer login em suas contas para comprar ingressos. 
Certificar que o processo de login está sendo fácil de usar e seguro, com autenticação de dois fatores, se possível.

Página de Compra de Ingressos: Depois de fazer login, os clientes podem acessar a página de compra de ingressos, onde selecionam o tipo de ingresso desejado e adicionam ao carrinho.

<h1>Back-end do Site (API):</h1>

Banco de Dados: Manter um banco de dados que acompanha os ingressos disponíveis e os vendidos. Cada ingresso deve ser vinculado a um cliente quando vendido.
Fila de Espera: Implementar uma fila de espera virtual para gerenciar as solicitações de compra. Os clientes são atendidos com base na ordem em que chegaram à fila.

<h1>IMPORTANTE!!!</h1>
</br>
<b>Sistema de Reservas: Quando um cliente seleciona um ingresso, este pode ser reservado por um curto período de tempo (por exemplo, 5-10 minutos) para evitar que outros clientes comprem o mesmo ingresso durante o processo de checkout.</b></br>


Rate Limiting: Implemente limites de taxa para impedir que um único cliente sobrecarregue o sistema com solicitações de compra. Isso garante que clientes com internet mais rápida não monopolizem os ingressos.


Transações Atômicas: Garanta que as transações de compra sejam atômicas, o que significa que elas são completamente bem-sucedidas ou completamente revertidas em caso de falha.

</br>

Ferramentas de Balanceamento de Carga: Use um sistema de balanceamento de carga para distribuir as solicitações de compra entre vários servidores ou instâncias para garantir que o site permaneça responsivo, mesmo durante picos de tráfego.

Notificações em Tempo Real: Implementar notificações em tempo real para informar os clientes sobre o status de sua compra, como confirmação de compra, rejeição devido à falta de ingressos, etc. (CRM)

Políticas de Vendas: Estabelecer políticas claras de venda, como limite de quantidade de ingressos por cliente e restrições para evitar a compra de ingressos em massa por meio de bots.
Monitoramento e Análise: Utilizar ferramentas de monitoramento para rastrear o desempenho do site, identificar gargalos e ajustar recursos conforme necessário. Analise os dados para melhorar a experiência do usuário. (GRAFANA)

Teste de Estresse: Realizar testes de estresse para simular picos de tráfego e verificar como o sistema lida com eles. Isso ajuda a identificar possíveis problemas de desempenho.

Backup e Recuperação: Ter planos de backup e recuperação para lidar com falhas inesperadas, garantindo a disponibilidade contínua do site durante a venda de ingressos.
Registro de Auditoria: Manter um registro de auditoria detalhado das transações para fins de prestação de contas e segurança.

