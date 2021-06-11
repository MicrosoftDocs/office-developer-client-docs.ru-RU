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
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422245"
---
# <a name="pidtagabproviderid-canonical-property"></a>Каноническое свойство PidTagAbProviderId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит структуру [MAPIUID поставщика адресных книг.](mapiuid.md) 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Идентификатор:  <br/> |0x3615  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Структура **MAPIUID** определяет, какой поставщик адресных книг поставляет этот контейнер в иерархии контейнеров. Значение уникально для каждого поставщика. 
  
Поставщик адресных книг может предоставить несколько идентификаторов. Например, поставщик, который поставляет два разных контейнера, может публиковать в PR_AB_PROVIDER_ID **уникальные** идентификаторы для каждого контейнера. 
  
 **PR_AB_PROVIDER_ID** аналогично свойству **PR_MDB_PROVIDER** [(PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)для магазинов сообщений. Клиентские приложения могут использовать **PR_AB_PROVIDER_ID** для поиска связанных строк в таблице иерархии адресных книг. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[Каноническое свойство PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

