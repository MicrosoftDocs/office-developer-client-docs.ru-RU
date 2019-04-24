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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315822"
---
# <a name="pidtagabproviderid-canonical-property"></a>Каноническое свойство PidTagAbProviderId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит структуру [мапиуид](mapiuid.md) поставщика адресных книг. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АБ_ПРОВИДЕР_ИД  <br/> |
|Идентификатор:  <br/> |0x3615  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Замечания

Структура **мапиуид** определяет, какой поставщик адресных книг предоставляет этот конкретный контейнер в иерархии контейнеров. Значение уникально для каждого поставщика. 
  
Поставщик адресных книг может предоставить несколько идентификаторов. Например, поставщик, который предоставляет два различных контейнера, может публиковать в **пр_аб_провидер_ид** уникальных идентификаторов для каждого контейнера. 
  
 **Пр_аб_провидер_ид** является аналогом свойства **пр_мдб_провидер** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) для хранилищ сообщений. Клиентские приложения могут использовать **пр_аб_провидер_ид** для поиска связанных строк в таблице иерархий адресной книги. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[Каноническое свойство PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

