
** Instalando o Git **

```python
sudo apt  install git
```
É necessário gerar uma chave ssh e fazer um cadastro em algum repositório git, por questões de segurança vamos criar uma chave:

```python
ssh-keygen -t rsa -C "comment"
```


** Comandos **

```git remote add <arquivos>```: adiciona um repositório ao git que foi iniciado neste diretório.

```git commit -m "comentário qualquer"```: Este comando realiza o que chamamos de “commit”, que significa pegar todos os arquivos que estão naquele lugar ```INDEX``` que o comando ```add``` adicionou e criar uma revisão com um número e um comentário, que será vista por todos.

```git status```: Exibe o status do seu repositório atual.

```git pull origin master```: Baixar(pull=puxar) o projeto para o projeto local.

```git checkout -b iss53```: Para trabalhar em uma issue específica e criar uma branch para as alterações antes de dar deploy no repositório master.

```git merge iss53```: Após rodar os testes e ter certeza que é a correção ou atualização que você quer, faça o merge no seu branch master para fazer deploy em produção.

```python
git checkout master
git merge iss53
```

```git push origin master```: Enviar(push=empurrar) o projeto para o repositório no GitHub.

```git clone```: Clona um projeto para a máquina que irá acessar o repositório.

```git commit --amend```: modifica a mensagem do commit mais recente, ou seja, o último commit feito por você no projeto. Além de você mudar a mensagem do commit, você consegue adicionar arquivos que você se esqueceu ou retirar arquivos comitados por engano. O git cria um commit totalmente novo e corrigido.

** Testando o uso do Git **

Criando arquivo:

```python
touch teste
```

Adicionando alterações:
1 - Somente uma alteração

```python
git add teste
```
2 - Todas alterações
```python
git add .
```

Neste passo as alterações ainda não estão sob o controle de versão, elas somente foram adicionadas para quando der um commit.

Comitar alterações:

```python
git commit -m "mensagem teste para o tutorial"
```

Se durante o tempo em que fez o pull e o push outra pessoa que também participe do projeto fez alterações o push será rejeitado. Então é necessário atualizar o projeto local antes de enviar novas alterações.

```python
git fetch origin
```
