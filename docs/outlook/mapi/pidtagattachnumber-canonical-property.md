---
title: Каноническое свойство PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327253"
---
# <a name="pidtagattachnumber-canonical-property"></a>Каноническое свойство PidTagAttachNumber

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит номер, однозначно определяя вложение в родительском сообщении. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_NUM  <br/> |
|Идентификатор:  <br/> |0x0E21  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилища сообщений создают и поддерживают это свойство. Номер вложения — это дополнительный ключ сортировки после позиции отрисовки в таблице вложений. 
  
 **PR_ATTACH_NUM** используется для открытия вложения с помощью метода [IMessage::OpenAttach.](imessage-openattach.md) В сеансе клиентского приложения  свойство PR_ATTACH_NUM сообщения остается постоянным, если открыта таблица вложений. 
  
Хранилище сообщений распространяет изменения в таблицу с помощью методов **IMessage::CreateAttach** и **IMessage::D eleteAttach.** При этом хранилище сообщений может создавать табличные уведомления в открытых таблицах вложений, чтобы клиенты могли повторно синхронизироваться с этими изменениями. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
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

