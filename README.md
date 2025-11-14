PROJETO - COLETA EFICAZ DE RESÍDUOS URBANOS
Enganheria de Descarte

Documentos constando na pasta do projeto
1) Link Figma - [https://www.figma.com/proto/Sd3FSDB82dyEBDxq52Rc3d/Untitled?node-id=1-76&starting-point-node-id=1%3A76&locale=pt-br&t=EmGLsldoXqkiu9zk-1]
2) Banco de dados em três formatos:
   a - sql;
   b - txt;
   c - Modelo lógico.
3) Documento - TAP
4) Readme.md - Link do Figma
5) Descrição completa do sistema

   Sistema de Gestão de Coleta de Resíduos

   O sistema de gestão de coleta de resíduos foi desenvolvido para facilitar o controle e a organização de todo o processo de coleta urbana. Ele funciona como uma plataforma web onde é possível gerenciar usuários, veículos, rotas, problemas operacionais e relatórios gerais. A ideia é que tudo fique centralizado em um único lugar, de maneira simples, intuitiva e acessível. A estrutura do sistema foi construída com Django, utilizando MySQL como banco de dados, além de HTML, CSS e Bootstrap para a interface.
   
   Por dentro, o sistema segue o padrão tradicional do Django: modelos que representam os dados, views que controlam as ações e páginas, templates responsáveis pela interface, formulários para entrada de dados e decoradores que garantem as permissões certas para cada usuário. Quando uma pessoa acessa alguma página, o Django identifica a URL, chama a função correspondente, consulta o banco de dados se necessário e devolve ao usuário a página já montada e funcional. Para começar a usar o sistema, basta instalar o Python, criar um ambiente virtual, instalar as dependências e configurar o MySQL. Depois disso, executam-se as migrações do banco e cria-se um superusuário, o que já habilita o sistema a funcionar normalmente através do comando padrão do Django para iniciar o servidor. A partir desse ponto, tudo já está pronto para ser acessado pelo navegador.
   
   A construção do sistema foi dividida em módulos. No app de usuários, cada pessoa registrada recebe automaticamente um perfil associado ao usuário padrão do Django. Existem três tipos principais de perfis: cidadão, gestor de rotas e administrador. Cada um deles tem níveis de acesso diferentes, garantindo que apenas quem realmente pode realizar determinada ação consiga fazê-lo. O login é realizado por email e senha, e o controle de permissões usa decoradores personalizados que bloqueiam ou liberam o acesso conforme o papel do usuário.
   No app de veículos e rotas estão concentradas as informações sobre os caminhões, caçambas e seus percursos. Cada veículo possui seus dados básicos cadastrados, como placa e tipo. Já as rotas determinam onde e quando a coleta será realizada, sempre associadas a um veículo específico. Também existe um módulo para registrar problemas relacionados ao serviço, como coleta não realizada, atrasos, falhas mecânicas, entre outros. Tudo isso pode ser visualizado, filtrado, editado ou excluído pelos gestores.
   
   O sistema também oferece uma área de relatórios, onde é possível ter uma visão geral da operação. Ali, o usuário consegue ver quantos veículos existem, quantos estão ativos, o número total de rotas, quantas foram concluídas e quais problemas foram registrados. Esses dados ajudam a entender o desempenho do serviço, identificar falhas e tomar decisões mais assertivas. As permissões foram estruturadas para garantir ordem e segurança. O cidadão tem acesso básico e pode registrar problemas relacionados à coleta. O gestor de rotas já possui um nível de acesso maior, podendo cadastrar veículos, rotas e gerenciar os problemas registrados. O administrador, por sua vez, tem controle total do sistema, incluindo a parte de usuários. Esse controle por níveis mantém a organização e evita alterações indevidas.

   Na prática, o fluxo é simples. O usuário acessa a página de login, insere email e senha e, se estiver tudo certo, é direcionado ao painel principal. A partir daí, quem é gestor ou administrador pode cadastrar novos veículos, criar rotas, marcar rotas como concluídas e visualizar ou solucionar problemas registrados. Já os cidadãos conseguem relatar situações como coleta não realizada, o que ajuda a equipe de gestão a acompanhar melhor o que está acontecendo na cidade.

Todo o sistema foi construído seguindo boas práticas, como organização por apps, validação de dados, reutilização de código e mensagens claras de retorno para o usuário. Apesar de já ser bastante funcional, ainda existe espaço para melhorias, como implementar uma API, adicionar exportação de relatórios em PDF ou Excel, integrar notificações por email e melhorar ainda mais a interface visual.
