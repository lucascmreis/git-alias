# Notes

Arquivo de configurações básicas para atalhos com git.

>Em construção

## git config

No git, existem basicamente 3 níveis de configuração

- config —system ⇒ afeta todos os usuários e projetos
- config —global ⇒ afeta todos os projetos de um usuário
- config —local ⇒ afeta apenas o repositório local

Para editar as configurações do git só rodar o comando

```jsx
git config --global --edit
```

Por padrão isso irá aparecer no editor vi. Se quiser mudar o editor padrão, basta alterar o core.editor e em seguida rodar o edit novamente.

```jsx
git config --global core.editor code
```

>Importante também passar a flag —wait no editor config, porque em alguns momentos, durante o carregamento do code isso pode gerar uma página em branco.

## git alias

Para adicionar alias para os comandos padrões do git e ajudar na produtividade:

1. No git config, incluir um campo [alias] e abaixo os atalhos
2. Lista de atalhos criados:

`//mostra o status de forma resumida`

s = !git status -s

`// realiza o add e commit, onde na pratica so precisa passar a mensagem`

c = !git add —all && git commit -m

`// mostra o log formatado`

l = !git log —pretty=format:'%C(blue)%h %C(red)%d%C(white)%s - %C(cyan)%cn, %C(green)%cr'


<br>
<aside>
💡 Para formatar o log com cores, basta usar <code>%C(nome-da-cor) </code>

</aside>
