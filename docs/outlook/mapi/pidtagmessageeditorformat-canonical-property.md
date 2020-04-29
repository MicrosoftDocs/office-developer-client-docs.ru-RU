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
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325636"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Каноническое свойство PidTagMessageEditorFormat

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает формат, используемый редактором для отображения сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Идентификатор:  <br/> |0x5909  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Возможные значения для **PR_MSG_EDITOR_FORMAT** могут быть одним из следующих: 
  
|**Значение**|**Описание**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Неизвестный формат используемого редактора.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |Редактор должен отображать сообщение в формате обычного текста.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |Редактор должен отображать сообщение в формате HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |Редактор должен отображать сообщение в формате RTF.  <br/> |
   
По умолчанию сообщения электронной почты (с классом сообщения **IPM. Примечание** или с настраиваемым классом сообщений, производным от **IPM. Note**), отправленные с учетной записи почты POP3/SMTP, отправляются в формате TNEF. Свойство **PR_MSG_EDITOR_FORMAT** можно использовать для применения только обычного текста, а не TNEF при отправке сообщения. Если для параметра **PR_MSG_EDITOR_FORMAT** задано значение **EDITOR_FORMAT_PLAINTEXT**, сообщение отправляется в виде обычного текста без формата TNEF. Если для параметра **PR_MSG_EDITOR_FORMAT** задано значение **EDITOR_FORMAT_RTF**, кодировка TNEF неявно включена, а сообщение отправляется с использованием формата Интернета по умолчанию, указанного в клиенте Outlook.
  
Существует два других способа применения формата TNEF при отправке сообщения.
  
- Если задать для свойства с именем **диспидусетнеф** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) значение true в сообщении, то при преобразовании сообщения из MAPI в MIME/SMTP необходимо включить формат TNEF. Обратите внимание, что **диспидусетнеф** применяется только в том случае, если сообщение отправлено с учетной записи электронной почты POP3/SMTP и не применяется, когда сообщение отправляется другими поставщиками, например Microsoft Exchange Server. **диспидусетнеф** переопределяет параметр в **PR_MSG_EDITOR_FORMAT**.
    
- Использование флага **CCSF_USE_TNEF** при вызове [Иконвертерсессион:: мапитомиместм](iconvertersession-mapitomimestm.md) для преобразования исходящего сообщения MAPI в MIME поток также может применять TNEF. Это свойство применяется, даже если **диспидусетнеф** не задано. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

