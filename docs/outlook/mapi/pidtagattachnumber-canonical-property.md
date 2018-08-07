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
ms.openlocfilehash: c4a46710311f2c4d26ec3d667c7bf535df69f595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810865"
---
# <a name="pidtagattachnumber-canonical-property"></a>Каноническое свойство PidTagAttachNumber

  
  
**Относится к**: Outlook 
  
Содержит номер, который уникальным образом определяет вложения в сообщении его родительского. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_NUM  <br/> |
|Идентификатор:  <br/> |0x0E21  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Хранилищ сообщений создания и обслуживания этого свойства. Число вложений — второй ключ сортировки, после положения, в таблице вложений. 
  
 **PR_ATTACH_NUM** используется для открытия вложения с помощью метода [IMessage::OpenAttach](imessage-openattach.md) . В рамках сеанса клиентского приложения со значением свойства **PR_ATTACH_NUM** вложения сообщения не изменяется до тех пор, пока открыта в таблице вложений. 
  
Хранилище сообщений распространяет изменения в таблицу с помощью методов **IMessage::CreateAttach** и **IMessage::DeleteAttach** . В его параметр хранилище сообщений может создавать уведомления в таблице в таблицах открыть вложение, чтобы клиенты можно синхронизировать на такие изменения. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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

