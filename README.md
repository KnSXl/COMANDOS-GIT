# COMANDOS-GIT

## Configuração

- `git config --global user.name "Seu Nome"`: Define o nome do usuário globalmente.
- `git config --global user.email "seu_email@exemplo.com"`: Define o email do usuário globalmente.
- `git config --global color.ui auto`: Habilita a colorização da saída do Git.
- `git config --global core.editor "nome_do_editor"`: Define o editor de texto padrão.

## Inicialização e Clonagem

- `git init`: Cria um novo repositório Git no diretório atual.
- `git clone [url]`: Clona um repositório remoto.

## Manipulação de Arquivos

- `git add [arquivo]`: Adiciona um arquivo específico à área de stage.
- `git add .`: Adiciona todos os arquivos modificados à área de stage.
- `git rm [arquivo]`: Remove um arquivo do diretório de trabalho e da área de stage.
- `git mv [arquivo_original] [novo_arquivo]`: Move ou renomeia um arquivo.

## Commit e Log

- `git commit -m "mensagem do commit"`: Cria um commit com uma mensagem.
- `git commit -a -m "mensagem do commit"`: Comita todas as mudanças monitoradas, pulando `git add`.
- `git log`: Mostra o histórico de commits.
- `git log --oneline`: Mostra o histórico de commits de forma resumida.

## Branching e Merging

### Comandos Básicos

- `git branch`: Lista todas as branches locais.
- `git branch [nome_da_branch]`: Cria uma nova branch.
- `git checkout [nome_da_branch]`: Muda para a branch especificada.
- `git checkout -b [nome_da_branch]`: Cria e muda para uma nova branch.
- `git merge [nome_da_branch]`: Faz merge da branch especificada na branch atual.
- `git branch -d [nome_da_branch]`: Deleta a branch especificada.

### Comandos Avançados

#### Branching

- `git branch -m [nome_novo]`: Renomeia a branch atual para `[nome_novo]`.
- `git branch -M [nome_novo]`: Força a renomeação da branch atual para `[nome_novo]`.
- `git branch --move [nome_antigo] [nome_novo]`: Renomeia uma branch de `[nome_antigo]` para `[nome_novo]`.
- `git branch -r`: Lista todas as branches remotas.
- `git branch -a`: Lista todas as branches, tanto locais quanto remotas.
- `git branch --merged`: Lista todas as branches que foram mescladas na branch atual.
- `git branch --no-merged`: Lista todas as branches que não foram mescladas na branch atual.

#### Merging

- `git merge --no-ff [nome_da_branch]`: Faz um merge da branch especificada na branch atual, sempre criando um commit de merge.
- `git merge --squash [nome_da_branch]`: Faz um merge das mudanças da branch especificada na branch atual, mas as coloca na área de stage sem criar um commit de merge.
- `git merge --abort`: Aborta um merge em andamento e restaura o estado da branch para antes do início do merge.
- `git merge --continue`: Continua o processo de merge após resolver conflitos.

#### Rebasing

- `git rebase -i [commit]`: Inicia uma rebase interativa a partir do commit especificado.
- `git rebase --onto [nova_base] [base_antiga] [branch]`: Rebase a `[branch]` para começar a partir de `[nova_base]` em vez de `[base_antiga]`.
- `git rebase --abort`: Aborta um rebase em andamento e restaura o estado da branch para antes do início do rebase.
- `git rebase --continue`: Continua o processo de rebase após resolver conflitos.

### Resolução de Conflitos

- `git mergetool`: Inicia uma ferramenta de merge visual para resolver conflitos de merge.
- `git diff --name-only --diff-filter=U`: Lista os arquivos com conflitos de merge.

### Branch Tracking

- `git branch --set-upstream-to=origin/[branch] [branch_local]`: Define a branch remota de upstream para a branch local.
- `git push --set-upstream origin [branch]`: Define a branch local como a branch de upstream para a branch remota e envia as mudanças.

### Manipulação de Commits em Branches

- `git cherry-pick [commit]`: Aplica um commit específico na branch atual.
- `git cherry-pick --abort`: Aborta um cherry-pick em andamento.
- `git cherry-pick --continue`: Continua o processo de cherry-pick após resolver conflitos.

### Branching Remoto

- `git push origin --delete [branch]`: Deleta uma branch remota.
- `git fetch origin`: Atualiza as referências remotas, mas não faz merge ou rebase.
- `git pull origin [branch]`: Faz pull das mudanças de uma branch remota específica.

## Atualização e Publicação

- `git fetch`: Baixa as mudanças do repositório remoto.
- `git pull`: Baixa e integra as mudanças do repositório remoto.
- `git push`: Envia as mudanças para o repositório remoto.
- `git push --set-upstream origin [nome_da_branch]`: Define a branch upstream e envia as mudanças.

## Stash e Restore

- `git stash`: Armazena temporariamente todas as mudanças locais.
- `git stash list`: Lista todas as stashes.
- `git stash apply`: Aplica a última stash armazenada.
- `git stash pop`: Aplica e remove a última stash.

## Inspeção e Comparação

- `git status`: Mostra o estado dos arquivos no diretório de trabalho e na área de stage.
- `git diff`: Mostra as diferenças não comitadas.
- `git diff [branch]`: Compara a branch atual com outra branch.

## Remoção e Resolução de Conflitos

- `git reset [arquivo]`: Remove um arquivo da área de stage.
- `git reset --hard [commit]`: Reseta o diretório de trabalho e a área de stage para um commit específico.
- `git clean -f`: Remove arquivos não rastreados.

## Reflog e Recuperação

- `git reflog`: Mostra um histórico de todas as referências (commits).
- `git revert [commit]`: Reverte um commit criando um novo commit que desfaz as mudanças.
