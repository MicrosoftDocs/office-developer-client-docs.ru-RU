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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, следует ли включать в сообщение формат TNEF, если сообщение преобразуется из формата MAPI в формат MIME или SMTP (Simple Mail Transfer Protocol).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидусетнеф  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008582  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Настройка времени выполнения  <br/> |
   
## <a name="remarks"></a>Примечания

Данное свойство указывает, следует ли включать TNEF в сообщение при преобразовании сообщения из формата TNEF в формат MIME или SMTP. Это свойство может отсутствовать, и если да, то не требуется включать в сообщение TNEF.
  
Это свойство применяется только в том случае, если сообщение отправлено с учетной записи электронной почты POP3/SMTP и не применяется при отправке сообщения другими поставщиками, такими как Microsoft Exchange Server.
  
В определенных обстоятельствах, например при включении кнопок голосования или при присоединении к сообщению внедренного объекта OLE, Outlook может установить это свойство, чтобы принудительно использовать формат TNEF.
  
Свойство **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) можно использовать для принудительного применения только обычного текста, а не TNEF при отправке сообщения. Так как **PidLidUseTNEF** переопределяет параметр в **PR_MSG_EDITOR_FORMAT**, то приложение, которое требуется принудительно использовать обычный текст в исходящих сообщениях, также должно искать **PidLidUseTNEF** и сбрасывать его в значение false. Кроме того, надстройка должна удалить функции сообщений, которые требовали формат TNEF, чтобы избежать непригодных для отправки сообщений. 
  
Используйте флаг **CCSF_USE_TNEF** при вызове [Иконвертерсессион:: мапитомиместм](iconvertersession-mapitomimestm.md) для преобразования исходящего сообщения MAPI в MIME поток также может применять TNEF. Это свойство применяется, даже если **PidLidUseTNEF** не задано. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

