---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330228"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ноль или более свойств, принадлежащих получателю.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> Резервирования должно быть равно нулю.
    
 **Квалуес**
  
> Количество свойств в массиве значений свойств, на которое указывает элемент **ргпропвалс** . Элемент **квалуес** может иметь значение 0. 
    
 **Ргпропвалс**
  
> Указатель на массив значений свойств, описывающий свойства получателя. Элемент **ргпропвалс** может иметь значение null. 
    
## <a name="remarks"></a>Комментарии

Структура **адрентри** описывает свойства, принадлежащие одному получателю. Ниже перечислены свойства, которые обычно используются для описания получателя. 
  
 **Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Если в массиве [спропвалуе](spropvalue.md) для получателя отображается идентификатор записи или свойство **пр_ентрид** , это указывает на то, что получатель разрешен. Клиенты вызывают метод [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) , чтобы убедиться, что все получатели в списке получателей исходящих сообщений разрешены. С сообщениями можно отправлять только разрешенных получателей. 
  
 Структуры **адрентри** , как правило, объединены в виде массива для элемента **аентриес** структуры [ADRLIST](adrlist.md) . 
  
 Структуры **адрентри** и структуры [сров](srow.md) идентичны, так как они содержат зарезервированный элемент, массив значений свойств и число значений в массиве. В то время как структуры **адрентри** объединены для формирования элемента **аентриес** структуры **ADRLIST** , структуры **сров** объединяются для создания **аров** члена структуры [SRowSet](srowset.md) . Оба типа структур следуют одним и тем же правилам выделения, подразумевая, что структура **SRowSet** , получаемая из таблицы содержимого контейнера адресной книги, может быть приведена к структуре **ADRLIST** и использоваться как есть. 
  
Структура **адрентри** может быть пустой. Например, структура **адрентри** , которая находится в структуре **ADRLIST** , на которую указывает параметр _лппадрлист_ при вызове **IAddrBook:: Address** может быть пустым при удалении получателя. 
  
Дополнительные сведения о том, как выделить память для структур **адрентри** , можно узнать в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>См. также



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Структуры MAPI](mapi-structures.md)

