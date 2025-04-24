# Hospital

HOSPITAL FUNDAMENTAL (em progresso)



Atividade PT.4 : Atualizar o bando de dados do Hospital, mostrando se o médico ainda atua no hospital ou não.
Como realizei: adicionando uma nova coluna no shell escrita "em_atividade" no documento. Será identificado como 'true' para ativo e 'false' para inativo.

```js
db.medicos.updateMany(
  {},
  { $set: { em_atividade: true } }
)
```
Agora, iremos fazer com que dois médicos fiquem inativos em nosso banco, atualizando o status deles dessa maneira: 

```js
db.medicos.updateOne(
  { crm: " " },
  { $set: { em_atividade: false } }
)

db.medicos.updateOne(
  { crm: " " },
  { $set: { em_atividade: false } }
)
```

Pensei em utilizar o 'db.collection.find()' para procurar dois médicos, mas ainda tenho uma certa dificuldade com consultas em banco de dados, então escolhi a dedo dois médicos aleatórios:

```js

crm
"568154-SP"
crm
"658942-BA"
```
.

ATIVIDADE PT. 5: 
