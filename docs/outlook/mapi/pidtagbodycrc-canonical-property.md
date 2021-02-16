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
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415182"
---
# <a name="pidtagbodycrc-canonical-property"></a>Каноническое свойство PidTagBodyCrc

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение проверки циклической избыточности (CRC) в тексте сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_BODY_CRC  <br/> |
|Идентификатор:  <br/> |0x0E1C  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилище сообщений может использовать любой алгоритм CRC, который PT_LONG значение. Оно должно вычислять это свойство как часть метода [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) когда свойство **PR_BODY** ([PidTagBody)](pidtagbody-canonical-property.md)было установлено в первый раз и всякий раз, когда оно было изменено.
  
Клиентские приложения **используют PR_BODY_CRC** для сравнения текстовых строк сообщений, содержащихся в PR_BODY свойствах или их вариантах.  С помощью этого свойства клиент может быстро и легко определить, когда текст сообщения изменился. Это может значительно добиться увеличения производительности, **PR_BODY_CRC** вместо получения PR_BODY из магазина сообщений и сравнения его с локальной версией.  
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

