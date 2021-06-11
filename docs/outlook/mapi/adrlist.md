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
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415917"
---
# <a name="adrlist"></a>ADRLIST

**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает нулевые или несколько свойств, принадлежащих одному или более получателям. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>"Участники"

**cEntries**
  
> Количество записей в массиве, указанном участником **aEntries.** 
    
**aEntries**
  
> Массив [структур ADRENTRY,](adrentry.md) одна структура для каждого получателя. 
    
## <a name="remarks"></a>Примечания

Структура **ADRLIST** содержит одну или несколько структур **ADRENTRY,** каждая из которых описывает свойства получателя. Получатель может быть неурегулирован. Это означает, что в массиве значений свойств отсутствует идентификатор входа. Разрешенный получатель означает, что **свойство PR \_ ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)включено. Как правило, у разрешенных получателей также есть **адрес электронной** почты PR_EMAIL_ADDRESS [(Свойство PidTagEmailAddress).](pidtagemailaddress-canonical-property.md) Однако адрес электронной почты не требуется. **Структуры ADRLIST** используются, например, для описания списка получателей исходя из сообщения и mapI для отображения записей в адресной книге. 
  
**Структуры ADRLIST** напоминают [структуры SRowSet,](srowset.md) используемые для представления строк в таблицах. На самом деле эти две структуры разработаны таким образом, чтобы их можно было использовать взаимозаменяемо. Оба содержат массив структур, описывающих группу свойств, и количество значений в массиве. Если в структуре **ADRLIST** массив содержит структуры [ADRENTRY,](adrentry.md) то в **структуре SRowSet** массив содержит [структуры SRow.](srow.md) **Структуры ADRENTRY** и **структуры SRow** идентичны в макете. Так как структуры **ADRLIST** и **SRowSet** следуют одним и тем же правилам распределения, структура **SRowSet,** извлекаемая из таблицы содержимого контейнера адресной книги, может быть отлита в структуру **ADRLIST** и использоваться как есть. 
  
На следующем рисунке показан макет **структуры ADRLIST.** 
  
**Компоненты ADRLIST**
  
![Компоненты ADRLIST компоненты](media/amapi_18.gif "ADRLIST")
  
Части **ADRENTRY** и [SPropValue](spropvalue.md) в структуре **ADRLIST** должны быть выделены и освобождены независимо от других частей. То есть каждая структура **SPropValue** должна выделяться отдельно после того, как память для структуры **ADRENTRY** была выделена и освобождена до того, как структура **ADRENTRY** будет освобождена. Эта независимость в обработке памяти позволяет получателям и отдельным свойствам получателей свободно добавляться или удаляться из списка адресов. 
  
Функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIFreeBuffer](mapifreebuffer.md) должны использоваться для выделения и бесплатного выделения структуры **ADRLIST** и всех ее частей. 
  
Если список получателей слишком велик, чтобы вписаться в память, клиенты могут вызвать [метод IMessage::ModifyRecipients](imessage-modifyrecipients.md) для работы с подмножество списка. Клиенты не должны использовать общие диалоговое окно адресной книги в этой ситуации. 
  
Дополнительные сведения о выделении памяти для структур **ADRENTRY** см. в рубрике Управление памятью [для структур ADRLIST и SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md) 
  
## <a name="see-also"></a>См. также

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Структуры MAPI](mapi-structures.md)

