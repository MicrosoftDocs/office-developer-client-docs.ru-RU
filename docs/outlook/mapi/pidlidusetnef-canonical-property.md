---
title: Каноническое свойство PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384985"
---
# <a name="pidlidusetnef-canonical-property"></a>Каноническое свойство PidLidUseTnef

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, следует ли включать транспорта Neutral Encapsulation формата TNEF на сообщение при преобразовании этого сообщения из MAPI в формат Multipurpose Internet Mail Extensions (MIME) или Simple Mail Transfer Protocol (SMTP).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidUseTNEF  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008582  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Конфигурация во время выполнения  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет, следует ли включать TNEF на сообщение при преобразовании этого сообщения из формата TNEF в формате MIME или SMTP. Это свойство может отсутствовать, и если да, TNEF не должны быть включены в окне сообщения.
  
Это свойство применяется только в том случае, когда сообщение отправляется с учетной записью электронной почты POP3/SMTP и не применяется, если сообщение отправляется с другими поставщиками, такими как Microsoft Exchange Server.
  
При определенных условиях, например, при голосования активируются кнопки или внедренные OLE объекта присоединены к сообщению Outlook этому свойству можно задать для принудительного использования формата TNEF.
  
Свойство **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) можно использовать для применения параметров только обычный текст и не TNEF при отправке сообщения. Так как **PidLidUseTNEF** переопределяет параметр **PR_MSG_EDITOR_FORMAT**, приложение, которое хочет принудительное обычного текста на исходящие сообщения следует искать **PidLidUseTNEF** и сбросить значение FALSE. Кроме того надстройки необходимо удалить функции сообщения, которые требуется TNEF во избежание могут использовать вложения в сообщение, которое отправляется и, наконец. 
  
Использование флаг **CCSF_USE_TNEF** при вызове [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для преобразования исходящих сообщений MAPI в MIME-поток также обеспечивают TNEF. Это относится даже в том случае, если не указано **PidLidUseTNEF** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

