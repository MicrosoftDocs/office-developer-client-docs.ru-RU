---
title: Каноническое свойство PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b634f815d2aedecc716227c6525b846db38ca869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811970"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Каноническое свойство PidTagStoreProvider

  
  
**Относится к**: Outlook 
  
Содержит заданный поставщиком [MAPIUID](mapiuid.md) структуру, указывающую тип хранилища сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MDB_PROVIDER  <br/> |
|Идентификатор:  <br/> |0x3414  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Идентификатор свойства  <br/> |
   
## <a name="remarks"></a>Замечания

Структура [MAPIUID](mapiuid.md) определяет тип хранилища сообщений. Значение вычисляется поставщиками хранилища сообщений на объектов хранилища сообщений и является уникальным для каждого поставщика. Он обычно используется при просмотре в таблице хранилища сообщений для поиска хранилище требуемого типа, таких как общие папки. 
  
Это свойство является аналогом свойство **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) для адресных книг. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

