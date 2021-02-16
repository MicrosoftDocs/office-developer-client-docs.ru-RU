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
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412053"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Каноническое свойство PidTagStoreProvider

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит определяемую поставщиком [структуру MAPIUID,](mapiuid.md) которая указывает тип хранения сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MDB_PROVIDER  <br/> |
|Идентификатор:  <br/> |0x3414  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства ID  <br/> |
   
## <a name="remarks"></a>Примечания

Структура [MAPIUID](mapiuid.md) определяет тип хранения сообщений. Значение вычисляется поставщиками хранилищей сообщений в объектах хранения сообщений и уникально для каждого поставщика. Обычно он используется для просмотра таблицы хранения сообщений, чтобы найти хранилище нужного типа, например общедоступные папки. 
  
Это свойство аналогично свойству **PR_AB_PROVIDER_ID** ([PidTagAbProviderId)](pidtagabproviderid-canonical-property.md)для адресных книг. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

