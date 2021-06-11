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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315423"
---
# <a name="pidlidusetnef-canonical-property"></a>Каноническое свойство PidLidUseTnef

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, следует ли включить формат транспортной нейтральной инкапсуляции (TNEF) в сообщение при преобразовании этого сообщения из MAPI в многоцелевые расширения интернет-почты (MIME) или простой протокол передачи почты (SMTP).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidUseTNEF  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008582  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Конфигурация времени запуска  <br/> |
   
## <a name="remarks"></a>Примечания

В этом свойстве указывается, следует ли включить TNEF в сообщение при преобразовании этого сообщения из TNEF в формат MIME или SMTP. Это свойство может отсутствовать, и если это так, то TNEF не должен быть включен в сообщение.
  
Это свойство применяется только тогда, когда сообщение отправляется из почтовой учетной записи POP3/SMTP и не применяется, когда сообщение отправляется другими поставщиками, например Microsoft Exchange Server.
  
При определенных обстоятельствах, например при включении кнопок голосования или присоединении встроенного объекта OLE к сообщению, Outlook может настроить это свойство, чтобы заставить использовать TNEF.
  
Свойство **PR_MSG_EDITOR_FORMAT** [(PidTagMessageEditorFormat)](pidtagmessageeditorformat-canonical-property.md)может использоваться для применения только простого текста, а не TNEF при отправке сообщения. Так как **PidLidUseTNEF** переопределяет параметр в **PR_MSG_EDITOR_FORMAT,** приложение, которое хочет задействовать простой текст в исходяном сообщении, также должно искать **PidLidUseTNEF** и сбросить его в FALSE. Кроме того, надстройка должна удалить функции сообщения, которые требовали TNEF, чтобы избежать неиспользоваемых вложений в отправленное сообщение. 
  
Использование **флага CCSF_USE_TNEF** при вызове [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для преобразования исходячего сообщения MAPI в поток MIME также может применять TNEF. Это применимо даже в том **случае, если набор PidLidUseTNEF** не установлен. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

