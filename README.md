# Instalação, Dicas e atalhos do Git e GitHub

<div align="center">
<img src="https://github.com/devicons/devicon/blob/master/icons/github/github-original-wordmark.svg" width="150" />
<img src="https://github.com/devicons/devicon/blob/master/icons/git/git-original-wordmark.svg" width="150" />
</div>

## Links úteis:
[Sintaxe basica do Markdown](https://www.markdownguide.org/basic-syntax/)<br>
[Documentação do Git](https://git-scm.com/docs/git/pt_BR)

### Começo de tudo

**Criação da conta e repositório**

- Crie a sua conta no GitHub: https://github.com/
- Após a criação da conta, hora de criar seu primeiro repositório (Há uma + na lateral direita superior, clique nele e haverá a opção. Escolha o nome, não pode haver espaços, então use _)
- Por norma da comunidade, marque a opção "create Readme.md", esse arquivo é padrão e será a descrição do seu repositório (Como esse readme.md aqui)
- Após a criação, mantenha aberta a página com o repositório criado, logo mais vamos precisar dele.

**Instalação do git/git bash no computador**

- **Se você usa** *Windows*
  - Acesse o site oficial e faça o download do instalador do GIT para Windows.
  - Depois de baixado, clique duas vezes no arquivo para iniciar o assistente de instalação.
  - Basta seguir as instruções na tela, clicando em Next. Ao término, clique em Finish para concluir com êxito a instalação.

- **Se você usa** *Linux*, assim como eu:
  - Debian/Ubuntu
   > sudo apt-get update
   > sudo apt-get install git

  - **Para Ubuntu, versão estável Git version**
  > add-apt-repository ppa:git-core/ppa # apt update; apt install git

  - **Fedora**
  > yum install git (up to Fedora 21)
  > dnf install git (Fedora 22 and later) 

- Para demais distros: https://git-scm.com/download/linux

**Após instalação:**
- Crie uma pasta, use o nome da usa preferência (Ela será seu repositório local)
- Clique com o botão direito do mouse e abra o gitbash ou o terminal dentro da pasta
- Antes de mais nada, vamos definir o usuário e seu nome, esses dados estarão nos commit(comentários que irão junto com as atualizações que fará)
  - Para isso, digite:
  > git config --global user.name "João Silva"
  > git config --global user.email "exemplo@seuemail.com.br"
- A partir daqui, com certeza será melhor acompanhar um vídeo curto, mas bem instrutivo que me ajudou a configurar a branch.
      - O objetivo principal de um branch é desenvolver novas funcionalidades, mantendo-os isolados uns dos outros.
      - O branch padrão em qualquer projeto é sempre o main branch
  > Configuração de Branch e primeiro commit(Resumo).: https://www.youtube.com/watch?v=MdthEusEoy8
  
- **Esse mini curso do Dev Aprender também me ajudou demais, dua menos 49 min, mas consigirá entender perfeitamente o que são Branch,Commits,como fazer o upload(Push) e o download(pull/clone) dos seus repositórios.**
  > Mini Curso Completo: https://www.youtube.com/watch?v=kB5e-gTAl_s&t=1822s



***Agora que você ja instalou e provavelmente já deu o primeiro commit e fez seu primeiro push, chegou a hora de algo mais avançado e que o ajudará a não ficar digitando a senha toda vez que for dar um push***

**Dicas para gerar chave SSH e associar email no Github** 

***Gerando chave no terminal do linux:***
1) ssh-keygen
2) Navegar até a pasta do arquivo id_rsa.pub
3) Ler o conteudo do arquivo no terminal (cat id_rsa.pub)
4) Copiar o conteúdo e colar no Github em configurações >> Chave SSH >> Nova Chave

***1) Criar chave SSH no GitBash***

  - $ ssh-keygen -t ed25519 -C "seu email aqui"

***2) Gerar chave para Github***

  - $ cat id_...   .pub

***3) Copiar e jogar no seu Github***

  - Entrar na área de configuraçoes .. segurança e criar uma nova chave SSH

  Voltar ao GitBash

***4) Validar no GitBash***

  - Ativar agente = $ eval $(ssh-agent -s)
  - Adicionar ao agente = $ ssh-add id_... (sem ser a .pub)

*Comando para verificar se o email e nickname estao associado ao Github:*

  - *Git config --list* (Verificar nome e nickname)

      - Para resetar a configuraçao:
        - Git config --global --unset user.email
        - Git config --global --unset user.nickname

      - Para associar novamente:
        - Git config --global user.email "seu email do Github"
        - Git config --global user.nickname "Seu nick no Github"





***Comandos mais usados no Git/Gitub***
 - *git status* - Verificar status da pasta e arquivos
  
 - *git add <arquivo>* - Adiciona só o arquivo especificado (Lembrar de colocar a extensão do arquivo)
  
 - *git add .* - adicionar todos os arquivos no repositorio(pasta) local
  
 - *git commit -m "sua descrição aqui"* - Escrevar um commit ou comentário sobre a versao a ser adicionada
  
 - *git push origin main* - Fazer push e enviar arquivos para o github
  
 - *git pull <repositório-remoto>* - Se você estiver no seu ambiente de trabalho e quiser atualizar a branch que está trabalhando!
  
 - *git branch <nome-da-branch>* - Esse comando criará uma branch em seu local de trabalho.
  
 - *git push -u <local-remoto> <nome-da-branch>* - Para fazer o push (algo como enviar) da nova branch para o repositório remoto
  
 - *git branch ou git branch --list* - Ver a lista de todas as branch (A que estiver com um * é a que você esta usando)
  
 - *git branch -d <nome-da-branch>* - Excluir uma branch
  
 - *git checkout <nome-da-branch>* - Para trabalhar em uma branch, primeiro, é preciso "entrar" nela. Usamos git checkout, na maioria dos casos, para trocar de uma branch para outra.
  
 - *git checkout -b <nome-da-branch>* - Comando de atalho que permite criar e automaticamente trocar para a branch criada ao mesmo tempo
