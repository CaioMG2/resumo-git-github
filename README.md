Git

O que é o git?
O Git é um sistema de controle de revisão de código aberto maduro e mantido ativo usado por milhares de desenvolvedores em todo o mundo.

Repositório: É onde o código será armazenado.

Configuração Git:
git config --global user.name/email

git config user.name/email (verificação)

git config init.defaultBranch (retorna a branch padrão)

Resumos e Comandos Gerais
Branch (Ramificar) e Merge (Fundir)

Clonar o repositório para um novo local:
git clone + link do repositório (nome opcional)

Gravar alterações no repositório:
git commit

"Puxar" as alterações do repositório remoto para o local (buscar e mesclar):
git pull

Mostrar o status da árvore de trabalho e área de preparação:
git status

Transformar o local em repositório Git:
git init

Mostrar o histórico do repositório:
git log

Criar uma pasta:
mkdir +'nome' (make directory)

Adicionar todos os arquivos:
git add .

Git Commit

Realizar commit com mensagem:
git commit -m 'mensagem'

Adicionar automaticamente todas as mudanças não rastreadas e modificadas e fazer o commit:
git commit -a -m 'mensagem'

Modificar o commit mais recente:
git commit --amend

Criar commit em arquivos específicos:
git commit file1.txt file2.txt -m "Mensagem do commit"

Realizar commit sem passar pela área de staging:
git commit -am

Área de Staging

1. Fazer Modificações:
   - Alterações feitas nos arquivos no diretório de trabalho.

2. Adicionar à Área de Staging:
   - Utilizar git add para incluir as modificações na área de staging.

3. Revisar as Alterações:
   - Usar git status para verificar as mudanças preparadas.

4. Criar o Commit:
   - Utilizar git commit para criar um commit com as alterações da área de staging.

Comando para adicionar mensagem de texto em um arquivo ou mostrar no terminal:
echo

Manter um diretório vazio:
git keep "convenção para manter um diretório vazio"

Excluir algo:
rm -rf "o que deseja excluir"

Desfazer Commit/Alterações

Git reset (--soft, --mixed, --hard):
   --soft: Mantém as mudanças no staging.
   --mixed: Remove as mudanças do staging, mantém no diretório de trabalho.
   --hard: Descarta completamente as mudanças não confirmadas.

Git restore:
   git restore <arquivo> (desfazer no diretório de trabalho)
   git restore --staged <arquivo> (desfazer da área de staging)

Acessar a Área de Staging

Utilizar git add para adicionar alterações.
Utilizar git status para verificar os arquivos na área de staging.
Utilizar git restore --staged <arquivo> para remover arquivos da área de staging.

Pull e Push

Git Pull:
   - Obter as alterações mais recentes de um repositório remoto e incorporá-las automaticamente ao branch local.

Git Push:
   - Enviar alterações locais para um repositório remoto, sincronizando o estado do branch local com o remoto.

Branch

Um branch no Git é uma ramificação independente do histórico de desenvolvimento em um repositório.
Permite trabalhar em novos recursos, correções de bugs ou experimentos sem afetar o branch principal.

Comandos Branch:
   - git branch: criar novos ramos
   - git checkout: mudar entre ramos
   - git merge: integrar mudanças
   - git checkout -b: criar e selecionar novos ramos
   - git branch -d ou -D: remover ramos

Renomear arquivo:
$ git mv <nome_antigo> <nome_novo>

Mover arquivo:
$ git mv <arquivo> <diretorio/>
