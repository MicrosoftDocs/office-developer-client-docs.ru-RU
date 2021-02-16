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
  
Указывает формат для редактора, который будет отображать сообщение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Идентификатор:  <br/> |0x5909  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Возможные значения **для** PR_MSG_EDITOR_FORMAT могут быть одним из следующих значений: 
  
|**Значение**|**Описание**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Формат используемого редактора неизвестен.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |В редакторе должно отображаться сообщение в обычном текстовом формате.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |Редактор должен отображать сообщение в формате HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |В редакторе должно отображаться сообщение в формате RICH Text.  <br/> |
   
По умолчанию сообщения электронной почты (с IPM класса **сообщений. Примечание** или с пользовательским классом сообщения, производным от **IPM. Примечание.** Отправленные из почтовой учетной записи POP3/SMTP, отправляются в формате TNEF. Свойство **PR_MSG_EDITOR_FORMAT** можно использовать для принудительного применения только обычного текста, а не TNEF при отправке сообщения. Если **PR_MSG_EDITOR_FORMAT** установлено **EDITOR_FORMAT_PLAINTEXT,** сообщение отправляется в виде обычного текста без TNEF. Если **PR_MSG_EDITOR_FORMAT** задан **EDITOR_FORMAT_RTF,** то кодирование TNEF неявно включено, и сообщение отправляется в интернет-формате по умолчанию, указанном в клиенте Outlook.
  
Существует два других способа принудительного использования TNEF при отправке сообщения.
  
- Если для именоваемой свойства **dispidUseTNEF** [(PidLidUseTnef)](pidlidusetnef-canonical-property.md)задайте для сообщения свойство True, это означает, что при преобразовании сообщения из MAPI в MIME/SMTP необходимо включить TNEF. Обратите внимание, что **dispidUseTNEF** применяется, только когда сообщение отправляется из почтовой учетной записи POP3/SMTP, и не применяется, когда сообщение отправляется другими поставщиками, например Microsoft Exchange Server. **dispidUseTNEF** переопределяет параметр **в** PR_MSG_EDITOR_FORMAT .
    
- Использование **флага CCSF_USE_TNEF** при вызове [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для преобразования исходячего сообщения MAPI в поток MIME также может применять TNEF. Это применимо, даже **если dispidUseTNEF** не заданной. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

