---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 87b91b66807ce79533029a8d5b5c4956bc4d5ce9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565769"
---
# <a name="adrlist"></a>ADRLIST

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описание ноль или больше свойств, относящихся к одному или нескольким получателям. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md) [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Число записей в массива, указанного параметром члена **aEntries** . 
    
**aEntries**
  
> Массив структур [ADRENTRY](adrentry.md) одной структуры для каждого получателя. 
    
## <a name="remarks"></a>Замечания

Структуру **ADRLIST** содержит один или несколько **ADRENTRY** структуры, каждый описанием свойства получателя. Получатель может быть нерешенные. Это означает, что она хватает идентификатор записи в его массив значений свойств. Разрешить получателя означает, что **связей с Общественностью\_ENTRYID** включено это свойство ([PidTagEntryId](pidtagentryid-canonical-property.md)). Как правило разрешенных получатели также быть сообщения электронной почты адрес свойство **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). Тем не менее адреса электронной почты не требуется. **ADRLIST** структуры используются, например, для описания списка получателей для исходящих сообщений и MAPI для отображения записей в адресной книге. 
  
**ADRLIST** структуры напоминать структур [SRowSet](srowset.md) структуры, используемые для представления строки в таблицах. На самом деле эти две структуры построены таким образом, чтобы они являются взаимозаменяемыми. Оба содержать массив структур, описывающих группы свойств и количество значений в массиве. В то время как в структуре **ADRLIST** массив содержит [ADRENTRY](adrentry.md) структуры, в структуре **SRowSet** массив содержит [SRow](srow.md) структуры. **ADRENTRY** структуры и структуры **SRow** идентичны в макете. Так как **ADRLIST** и **SRowSet** структур выполните те же правила распределения, структуру **SRowSet** , полученной из таблицы содержимого контейнера адресной книги можно привести к структуре **ADRLIST** и использовать. 
  
На следующем рисунке показана структура **ADRLIST** . 
  
**Компоненты ADRLIST**
  
![Компоненты ADRLIST] (media/amapi_18.gif "Компоненты ADRLIST")
  
**ADRENTRY** и [SPropValue](spropvalue.md) частями в структуре **ADRLIST** необходимо выделить и освободить независимо от других частей. То есть каждая структура **SPropValue** необходимо выделить по отдельности, после памяти для структуры **ADRENTRY** выделить и освободить перед освобождается структуры **ADRENTRY** . Эта независимость в обработке памяти позволяет свободно добавить или удалить из списка адресов получателей и отдельных параметров учетной записи получателя. 
  
Функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIFreeBuffer](mapifreebuffer.md) должен использоваться выделять и освобождать структуры **ADRLIST** и все его части. 
  
Если список получателей слишком велик для размещения в памяти, клиенты могут вызывать метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) для работы с подмножество списка. Клиенты не следует использовать адресной книги окон в этой ситуации. 
  
Дополнительные сведения о том, как выделить память для структуры **ADRENTRY** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>См. также

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Структуры MAPI](mapi-structures.md)

