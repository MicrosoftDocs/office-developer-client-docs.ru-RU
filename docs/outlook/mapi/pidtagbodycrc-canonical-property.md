---
title: Каноническое свойство PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810906"
---
# <a name="pidtagbodycrc-canonical-property"></a>Каноническое свойство PidTagBodyCrc

  
  
**Относится к**: Outlook 
  
Содержит значение суммы циклической на текста сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_BODY_CRC  <br/> |
|Идентификатор:  <br/> |0x0E1C  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Замечания

Хранилище сообщений можно использовать любой контрольной СУММЫ алгоритм, который создает значение PT_LONG. Его следует вычислять это свойство как часть метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) при **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) свойство имеет значение в первый раз, а также при последующем был изменен.
  
Клиентское приложение использует **PR_BODY_CRC** для облегчения сравнения строк текста сообщения, содержащихся в **PR_BODY** свойств или их варианты. При использовании этого свойства клиента можно быстро и легко обнаруживать при изменении текста сообщения. Его можно реализовать высокую производительность с помощью **PR_BODY_CRC** вместо получения **PR_BODY** хранилища сообщений и сравнение с локальной версией. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)
