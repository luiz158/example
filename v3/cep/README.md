# CEP App
Aplicação "Consulta CEP" com Demoiselle v3.0.

- **Auth**: (CRUD)
- **Cep**: Open

Verificação de segurança da api (https://schd.io/2sGy)

# Apps de exemplo

https://cep-fwkdemoiselle.rhcloud.com/ (Servidor Wildfly API)

# Exemplos de consulta (Restful padrão)

```bash
Lista de UF
https://cep-fwkdemoiselle.rhcloud.com/api/v1/ufs

Lista de Localidades por UF
https://cep-fwkdemoiselle.rhcloud.com/api/v1/cidades/PR
```

# Exemplos de consulta (Usando componente CRUD)

 ```bash
 Filtro por Logradouros do Paraná (PR)
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cep=80520270
  
 Filtro por Logradouros do Paraná (PR)
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?uf=PR
 
 Filtro por Logradouros do Paraná (Curitiba)
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cidade=Curitiba
 
 Filtro por Logradouros do Paraná (Curitiba) com apenas 11 registros
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cidade=Curitiba&range=0-10
 
 Filtro por Logradouros do Paraná (Curitiba) ordenado por logradouro
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cidade=Curitiba&sort=logradouro
 
 Filtro por Logradouros do Paraná (Curitiba) ordenado por bairro
 https://cep-fwkdemoiselle.rhcloud.com/api/v1/ceps?cidade=Curitiba&sort=bairroIni
```

# Instalação

```bash
# Baixar o repositório
git clone https://github.com/demoiselle/example.git --depth=1
```

## Backend
```bash
# Instalar Java 8 

# Instalar o maven 3

# Acessar a pasta "backend"
cd example/v3/cep/backend

# Fazer o build
mvn clean package -Pwildfly-swarm

# Inicia a aplicação (backend)
java -jar -Xmx128m target/cep-swarm.jar

# Acesse: http://localhost:8080/

```

## Frontend - Progressive (Angular 1.5)
```bash
# Instalar nvm (https://github.com/creationix/nvm)

# Instalar NodeJS (atualmente v7.1.x)
nvm install stable

# Instalar 
npm install -g bower grunt-cli 

# Acessar a pasta "progressive"
cd example/v3/cep/progressive

# Inicia a aplicação 
grunt serve

# Acesse: http://localhost:9000/
```
https://www.gitbook.com/@demoiselle

* https://play.google.com/store/apps/details?id=org.demoiselle.cep (não implementado)
