**Git:**

O Git é um sistema de controle de revisão de código aberto maduro e mantido ativo usado por milhares de desenvolvedores em todo o mundo.

Repositório: É onde o código será armazenado.

**Configuração Git:**

- `git config --global user.name/email`
- `git config user.name/email` (verificação)
- `git config init.defaultBranch` (retorna a branch padrão)

**Resumos e Comandos Gerais:**

**Branch (Ramificar) e Merge (Fundir):**

- Clonar o repositório para um novo local: `git clone + link do repositório` (nome opcional)
- Gravar alterações no repositório: `git commit`
- "Puxar" as alterações do repositório remoto para o local (buscar e mesclar): `git pull`
- Mostrar o status da árvore de trabalho e área de preparação: `git status`
- Transformar o local em repositório Git: `git init`
- Mostrar o histórico do repositório: `git log`
- Criar uma pasta: `mkdir +'nome'` (make directory)
- Adicionar todos os arquivos: `git add .`

**Git Commit:**

- Realizar commit com mensagem: `git commit -m 'mensagem'`
- Adicionar automaticamente todas as mudanças não rastreadas e modificadas e fazer o commit: `git commit -a -m 'mensagem'`
- Modificar o commit mais recente: `git commit --amend`
- Criar commit em arquivos específicos: `git commit file1.txt file2.txt -m "Mensagem do commit"`
- Realizar commit sem passar pela área de staging: `git commit -am`

**Área de Staging:**

1. Fazer Modificações:
   - Alterações feitas nos arquivos no diretório de trabalho.
   
2. Adicionar à Área de Staging:
   - Utilizar git add para incluir as modificações na área de staging.
   
3. Revisar as Alterações:
   - Usar git status para verificar as mudanças preparadas.
   
4. Criar o Commit:
   - Utilizar git commit para criar um commit com as alterações da área de staging.

**Comando para adicionar mensagem de texto em um arquivo ou mostrar no terminal:**
- `echo`

**Manter um diretório vazio:**
- `git keep "convenção para manter um diretório vazio"`

**Excluir algo:**
- `rm -rf "o que deseja excluir"`

**Desfazer Commit/Alterações:**

Git reset (--soft, --mixed, --hard):
   - --soft: Mantém as mudanças no staging.
   - --mixed: Remove as mudanças do staging, mantém no diretório de trabalho.
   - --hard: Descarta completamente as mudanças não confirmadas.

Git restore:
   - `git restore <arquivo>` (desfazer no diretório de trabalho)
   - `git restore --staged <arquivo>` (desfazer da área de staging)

**Acessar a Área de Staging:**

- Utilizar git add para adicionar alterações.
- Utilizar git status para verificar os arquivos na área de staging.
- Utilizar git restore --staged <arquivo> para remover arquivos da área de staging.

**Pull e Push:**

**Git Pull:**
   - Obter as alterações mais recentes de um repositório remoto e incorporá-las automaticamente ao branch local.

**Git Push:**
   - Enviar alterações locais para um repositório remoto, sincronizando o estado do branch local com o remoto.

**Branch:**

Um branch no Git é uma ramificação independente do histórico de desenvolvimento em um repositório. Permite trabalhar em novos recursos, correções de bugs ou experimentos sem afetar o branch principal.

**Comandos Branch:**
   - git branch: criar novos ramos
   - git checkout: mudar entre ramos
   - git merge: integrar mudanças
   - git checkout -b: criar e selecionar novos ramos
   - git branch -d ou -D: remover ramos

**Renomear arquivo:**
- `$ git mv <nome_antigo> <nome_novo>`

**Mover arquivo:**
- `$ git mv <arquivo> <diretorio/>`

**Stashs:**

Salvar as modificações atuais para prosseguir com outra abordagem de solução mas não perder o código: `git stash`

Verificar stashs criadas: `git stash list`

Recuperar stash criada: `git stash apply <nome>`

Limpar totalmente as stashs de uma branch: `git stash clear`

Remover uma stash específica: `git stash drop <nome>`

**Tags:**

Tags são utilizadas como um checkpoint de um branch.

Criar nova tag: `git tag <nome>`

Criar tag com mensagem: `git tag -a <nome> -m "mensagem"`

Listar tags: `git tag`

Ver tag específica: `git show <nome da tag>`

Trocar de tag: `git checkout <nome da tag>`

Enviar uma tag para o repositório: `git push origin <nome da tag>` ou para enviar mais tags: `git push origin --tags`

**Git Fetch:**

Atualiza todas as branches e tags.

**Submódulo:**

Maneira de trabalhar com dois ou mais projetos em um único repositório.

Adicionar submódulo: `git submodule add <repo>`

Verificar submódulos: `git submodule`

Atualizar um submódulo:

Primeiro, commitar as mudanças;
Enviar o repositório do submódulo: `git push --recurse-submodules=on-demand`

**Git Diff:**

Mostra a diferença entre branches ou arquivos.

**Comando git checkout -b:**

Cria uma nova branch e muda para ela.

**Git Shortlog:**

Log resumido do projeto, separado por autores.

**Otimização:**

- Limpar arquivos untracked: `git clean`
- Git GC (Garbage Collect): Identifica e exclui arquivos desnecessários.
- Git Fsck: Verifica a integridade de arquivos no repositório.
- Git Reflog: Mapeia seus passos no repositório, incluindo mudanças de branches.
- Git Archive: Transforma um repositório em um arquivo compactado: `git archive --format zip -o output.zip master`

**GitHub:**

Verificar licença e código-fonte.

**Aba Issue:**

Criar tarefas ou relatar bugs, usar Markdown no texto.

**Aba Pull Request:**

Colaboradores enviam código para resolver issues ou adicionar funcionalidades. Código é revisado antes de ser adicionado à branch principal. Pull requests vêm de branches separados e são revisados antes da integração.

**GitHub Recursos:**

**Abas:**

1. **Actions:**
   - Criar automações de deploy com integração a outros serviços.
   - Incluindo CI (Continuous Integration) e CD (Continuous Development).

2. **Projects:**
   - Criar projetos e utilizar um quadro de tarefas (Kanban).
   - Organizar o time com notas que se tornam issues.
   - Estrutura: Backlog > Retorno de Qualidade > Desenvolvimento > Teste > Finalizadas.

3. **Wiki:**
   - Criar documentação extensa para o projeto.
   - Descrever funcionalidades, bugs conhecidos, etc.
   - Repositório de conhecimento sobre o projeto.

4. **Insights:**
   - Informações detalhadas do projeto: contribuidores, commits, forks, etc.
   - Importante para entender a evolução do projeto.

5. **Settings:**
   - Acesso a diversas configurações do projeto.
   - Alterar nome dos repositórios, adicionar/remover features.
   - Gerenciar colaboradores e repositórios.

**Gist:**

Pequenos blocos de código hospedados no GitHub. Armazenar soluções para problemas que não devem ser perdidas. Links compartilháveis, funcionando como repositórios.

**GitHub Uso:**

- **Star:**
   - Marcar projetos que gostou.

- **Fork:**
   - Copiar projetos para repositório próprio.

GitHub oferece uma variedade de recursos para colaboração, automação e gerenciamento de projetos.

**Markdown no GitHub:**

Markdown é uma forma de adicionar estilo a textos na web. O arquivo README.md aceita markdown. Isso proporciona uma experiência melhor ao usuário em suas documentações.

**Cabeçalho:**

Os cabeçalhos são determinados pelo símbolo '#'. Similar aos headings do HTML: # é equivalente a h1, ## é equivalente a h2, e assim por diante.

**Ênfase no Texto:**

- Negrito: **texto**
- Itálico: *texto*

**Listas:**

- Lista não ordenada: * item
- Lista ordenada: 1. item

**Imagem:**

Para inserir uma imagem: ![texto](link da imagem). A imagem pode estar no repositório ou em um link externo.

**Link:**

Para inserir um link: [texto do link](link).

No próprio GitHub, você pode inserir código usando a sintaxe: \```código\```

**Fim do Resumo.**
