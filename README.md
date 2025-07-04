- **Nº do Squad: 12**

- **Integrantes:**

1. Elzilane Cardoso Barreto
2. Hirislayne Batista Ramos dos Santos
3. Isabella Castro Silva de Aguiar
4. Andiara Passos de Sousa Rios
5. Fernanda Aline Ferreira Alves de Souza
   -----
   
## Tecnologias Utilizadas no Backend (`aguiarisabela/maternidade-backend`)

### Principais Tecnologias

- **Java (27,9%)**
  - É a principal linguagem de programação utilizada no backend. Responsável por toda a lógica de negócio, processamento de dados, validações, segurança, autenticação/autorização, e por expor APIs REST que são consumidas pelo frontend.
  - O Java provavelmente utiliza frameworks como Spring Boot ou similares para simplificar o desenvolvimento de endpoints, gerenciamento de dependências, conexão com banco de dados e configuração do servidor web.
  - Toda a manipulação dos dados recebidos do frontend, as regras para persistência no banco e o retorno das respostas são centralizadas aqui.

- **HTML (46,2%)**
  - Utilizado em templates de páginas administrativas, páginas de login, dashboards internos ou telas de erro que são servidas diretamente pelo backend.
  - Também pode ser usado no envio de e-mails e na geração de relatórios ou outros recursos visuais administrativos.

- **CSS (23,8%)**
  - Utilizado para estilização dessas páginas administrativas ou templates HTML, garantindo uma apresentação visual agradável e organizada para os usuários das áreas internas do sistema.

- **JavaScript (2,1%)**
  - Provavelmente utilizado para adicionar interatividade em páginas administrativas servidas pelo backend, como validações de formulário, notificações, ou integração dinâmica nos templates HTML.

---

### Integração Entre as Tecnologias

O backend funciona como um servidor de aplicação, centralizando toda a lógica de negócio e o acesso ao banco de dados. Ele expõe endpoints (normalmente APIs REST) que recebem requisições HTTP do frontend (projeto `maternidade-recode`). O fluxo de integração é o seguinte:

1. **Recepção das Requisições:** O frontend envia requisições HTTP (GET, POST, PUT, DELETE) para URLs específicas mantidas pelo backend.
2. **Processamento:** O backend, em Java, processa essas requisições, aplica as regras de negócio, acessa o banco de dados conforme necessário e prepara uma resposta.
3. **Resposta:** Os dados são retornados geralmente no formato JSON, mas em alguns casos o backend pode servir páginas HTML completas (especialmente para áreas administrativas).
4. **Exibição/Atualização:** O frontend consome esses dados, atualiza a interface do usuário e exibe as informações solicitadas.

O HTML, CSS e JavaScript presentes no backend são normalmente restritos a áreas administrativas, relatórios, páginas de autenticação ou mensagens de erro, enquanto toda a comunicação programática com o frontend ocorre via APIs.

---

## Integração com o Frontend (`aguiarisabela/maternidade-recode`)

O frontend é responsável pela experiência do usuário final, coleta de informações e exibição dos dados processados pelo backend. Ele se comunica constantemente com o backend através de requisições HTTP. O fluxo típico é:

- O usuário realiza uma ação na interface do frontend.
- O frontend envia uma requisição HTTP para o backend.
- O backend processa e retorna uma resposta (dados, confirmação, erro, etc.).
- O frontend interpreta a resposta e atualiza a interface do usuário.

Toda a integração é realizada por meio de APIs REST, utilizando formatos padronizados (como JSON). O frontend consome apenas os dados necessários e exibe de forma interativa e responsiva, enquanto o backend garante a integridade, segurança e persistência das informações.

---

## Resumo do Funcionamento Integrado

- **Frontend (`maternidade-recode`)**: Executa no navegador do usuário, manipula a interface, coleta dados e envia requisições HTTP.
- **Backend (`maternidade-backend`)**: Processa requisições, executa lógicas de negócio em Java, acessa o banco de dados, retorna respostas ao frontend e serve páginas/administração quando necessário.
- **Comunicação**: Realizada via HTTP, com o frontend consumindo endpoints expostos pelo backend, garantindo uma separação clara entre apresentação (frontend) e lógica/processamento de dados (backend).

---

**Resumo para README:**

> O backend do projeto Maternidade é desenvolvido majoritariamente em Java, responsável por toda a lógica de negócio, processamento de dados e integração com o banco de dados. Também serve páginas administrativas utilizando HTML, CSS e JavaScript para funcionalidades internas. Toda a comunicação com o frontend é realizada através de APIs REST, garantindo escalabilidade, segurança e performance para a aplicação.
