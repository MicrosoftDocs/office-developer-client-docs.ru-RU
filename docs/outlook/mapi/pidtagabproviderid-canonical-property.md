---
title: Каноническое свойство PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f3aad4a5b3ba815d3e4f91e990bb63d75502f94b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580077"
---
# <a name="pidtagabproviderid-canonical-property"></a>Каноническое свойство PidTagAbProviderId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит структуру [MAPIUID](mapiuid.md) поставщика адресных книг. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Идентификатор:  <br/> |0x3615  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Замечания

Структура **MAPIUID** определяет, какой поставщик адресной книги предоставляет этот контейнер определенный в иерархии контейнеров. Значение является уникальным для каждого поставщика. 
  
Поставщика адресных книг можно обеспечить более одного идентификатора. Например поставщика, который предоставляет два разных контейнеров можно опубликовать **PR_AB_PROVIDER_ID** уникальных идентификаторов для каждого контейнера. 
  
 **PR_AB_PROVIDER_ID** является аналогом свойства **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) для хранилищ сообщений. Клиентские приложения могут использовать **PR_AB_PROVIDER_ID** для поиска строк, связанных с ними в иерархии таблицы адресной книги. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[Каноническое свойство PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

