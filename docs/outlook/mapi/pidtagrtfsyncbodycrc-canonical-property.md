---
title: Каноническое свойство PidTagRtfSyncBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357871"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a>Каноническое свойство PidTagRtfSyncBodyCrc

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит циклическую проверку избыточности (CRC), рассчитанную для текста сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РТФ_СИНК_БОДИ_КРК  <br/> |
|Идентификатор:  <br/> |0x1006  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Сообщение MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Функция [ртфсинк](rtfsync.md) вычисляет CRC, используя только те символы, которые она считает значимыми для сообщения. Например, в CRC пропускаются некоторые пробелы и другие игнорируемые символы. 
  
Это свойство является дополнительным свойством в формате RTF. Эти свойства используются функцией **ртфсинк** и не предназначены для непосредственного использования клиентскими приложениями. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

