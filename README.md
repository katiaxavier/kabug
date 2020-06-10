# kabug
Repositorio para testes com jenkins

## Como executar o projeto

* Importante ter o Ruby instalado (versão 2.5 ou superior)

### Instalar o Bundler
`
gem install bundler
`

### Instalar as dependencias do Ruby (projeto)
`
bundle install
`

### Executar localmente (minha maquina)
`
bundle exec cucumber
`

### Executar no servidor CI (gerando reposts JSON)
`
bundle exec cucumber -pi ci
`
