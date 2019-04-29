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
  
Содержит циклическую проверку избыточности (CRC) текста сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_БОДИ_КРК  <br/> |
|Идентификатор:  <br/> |0x0E1C  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Exchange;  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилище сообщений может использовать любой алгоритм CRC, который создает значение ПТ_ЛОНГ. Это свойство должно быть вычислено в составе метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , если свойство **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)) задано в первый раз и когда оно было изменено позже.
  
Клиентское приложение использует **пр_боди_крк** для упрощения сравнения текстовых строк сообщений, которые хранятся в свойствах **пр_боди** или их вариантах. С помощью этого свойства клиент может быстро и легко обнаружить, когда изменился текст сообщения. Использование **пр_боди_крк** вместо получения **пр_боди** из хранилища сообщений и его сравнения с локальной версией может значительно повысить производительность. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

