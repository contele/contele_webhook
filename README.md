
# Sobre webhooks

Os webhooks permitem que você construa ou configure integrações, como  Contele Hook, que assinam certos eventos no sistema Contele. Quando um desses eventos é acionado, enviaremos uma carga de POST por HTTP POST para a URL de configuração do webhook. Os webhooks podem ser usados para atualizar um dado externo ou alguma automação. A sua imaginação é o único limite.

### Configurando
1. Acesse a Pagina Integração
2. Acesse a aba webhook
3. Siga a instruções cole sua (URL) de destino e salve.

**Obs: 
A cada ação no Sistema sera enviado um evento para a URL de destino.**
**Como fazer para busca um único evento ou demais em específico?** 
**Leia a lista de eventos a baixo, filtre e busque evento desejado.**

### Events

```
form_anwsered
	Evento de formulario respondido.
task_created
	Evento de visita criada.
task_updated
	Evento de visita alterada.
task_deleted
	Evento de visita deletada
user_created
	Evento de usuario criado.
subordinates_updated
	Evento de carteira de usuarios alterada.
poi_created
	Evento de Local criado.
poi_updated
	Evento de Local alterado.
poi_deleted
	Evento de Local deletado.
```

### Fluxograma 
![mermaid-diagram-20220318161807](https://user-images.githubusercontent.com/33947194/159073363-ed9b286d-1302-4c90-a7c3-3652987222a2.png)

### Respostas
```
"hook_type"
    form_anwsered
    task_created
    task_updated
    task_deleted
    user_created
    subordinates_updated
    poi_created
    poi_updated
    poi_deleted
"data"
    "poi"
        id 
        customId 
        name 
        corporateName 
        cnpj_cpf 
        lat 
        lng 
        status 
        address 
        contacts 
        createdAt 
        updatedAt 
        categoryId 
        categoryName,
        creator_email,
        creator_id
    "task"
        id 
        poiId 
        customId 
        foreignOs 
        customPoiId 
        userId 
        timezone 
        datetime 
        withTime 
        status 
        checkoutTime 
        checkinTime 
        observation 
        comments 
        justification 
        os 
        createdAt 
        updatedAt 
    "user"
        id 
        name 
        username  
```
