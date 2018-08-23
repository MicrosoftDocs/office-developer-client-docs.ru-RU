---
title: Каноническое свойство PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c9c12d3e8314dea5be67727d0f286e7df13038fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574372"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Каноническое свойство PidTagMessageEditorFormat

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Задает формат для редактор, используемый для отображения сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Идентификатор:  <br/> |0x5909  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Возможные значения для **PR_MSG_EDITOR_FORMAT** может иметь одно из следующих: 
  
|**Значение**|**Описание**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Формат редактора использовать неизвестен.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |Редактор должны отображать сообщения в формате обычного текста.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |Редактор должны отображать сообщения в формате HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |Редактор должны отображать сообщения в формате RTF.  <br/> |
   
По умолчанию почтовые сообщения (с классом сообщения **IPM. Примечание** или с помощью настраиваемого сообщения класс, производный от **IPM. Обратите внимание на то**) отправляются из почты POP3/SMTP учетной записи, передаются в транспорта Neutral Encapsulation формата TNEF. Свойство **PR_MSG_EDITOR_FORMAT** можно использовать для применения параметров только обычный текст и не TNEF при отправке сообщения. Если **PR_MSG_EDITOR_FORMAT** **EDITOR_FORMAT_PLAINTEXT**, сообщение отправляется в виде обычного текста без TNEF. Если **PR_MSG_EDITOR_FORMAT** **EDITOR_FORMAT_RTF**, кодировка TNEF неявно включен, а сообщение отправляется в формате Интернета по умолчанию, который указан в клиенте Outlook.
  
Существует два способа внедрить использование TNEF при отправке сообщения.
  
- Параметр **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) с именем значение True для сообщения указывает, что TNEF должны быть включены при преобразовании сообщения из MAPI MIME/SMTP. Обратите внимание, что этот **dispidUseTNEF** применяется только в том случае, когда сообщение отправляется с учетной записью электронной почты POP3/SMTP и не применяется, если сообщение отправляется с другими поставщиками, такими как Microsoft Exchange Server. **dispidUseTNEF** переопределяет параметр **PR_MSG_EDITOR_FORMAT**.
    
- С помощью флага **CCSF_USE_TNEF** при вызове [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для преобразования исходящих сообщений MAPI в MIME-поток также обеспечивают TNEF. Это относится даже в том случае, если не указано **dispidUseTNEF** . 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет структуры основных данных, которые используются для удаленных операций.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
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

