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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421440"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает ноль или больше свойств, принадлежащих получателю.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a>"Участники"

 **ulReserved1**
  
> Зарезервировано; должно быть нулем.
    
 **cValues**
  
> Количество свойств в массиве значений свойств, на которые указывает **член rgPropVals.** Значением **члена cValues** может быть ноль. 
    
 **rgPropVals**
  
> Указатель на массив значений свойств, описывающий свойства получателя. Членом **rgPropVals** может быть NULL. 
    
## <a name="remarks"></a>Примечания

Структура **ADRENTRY** описывает свойства, принадлежащие одному получателю. К свойствам, которые обычно используются для описания получателя, относятся следующие: 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)
  
 **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)
  
Если идентификатор записи или **PR_ENTRYID** в массиве [SPropValue](spropvalue.md) для получателя, это означает, что получатель был разрешен. Клиенты звонят [методу IAddrBook::ResolveName,](iaddrbook-resolvename.md) чтобы убедиться, что все получатели в списке получателей исходяния сообщения разрешены. Отправлять сообщения могут только разрешенные получатели. 
  
 **Структуры ADRENTRY** обычно объединяются в массив для члена **aEntries** структуры [ADRLIST.](adrlist.md) 
  
 **Структуры ADRENTRY** и [структуры SRow](srow.md) идентичны, так как они содержат зарезервированный член, массив значений свойств и количество значений в массиве. В то время как структуры **ADRENTRY** объединяются для формирования члена **aEntries** структуры **ADRLIST,** структуры **SRow** объединяются для формирования **члена aRow** структуры [SRowSet.](srowset.md) Оба типа структур следуют одним и тем же правилам выделения, подразумевая, что структуру **SRowSet,** извлекаемую из таблицы содержимого контейнера адресной книги, можно привести к структуре **ADRLIST** и использовать как есть. 
  
Структура **ADRENTRY может** быть пустой. Например, структура **ADRENTRY,** которая содержится в структуре **ADRLIST,** на которую указывает параметр  _lppAdrList_ при вызове **IAddrBook::Address,** может быть пустой при удалении получателя. 
  
Дополнительные сведения о выделении памяти для структур **ADRENTRY** см. в под управлением памятью [для ADRLIST и структур SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md)
  
## <a name="see-also"></a>См. также



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Структуры MAPI](mapi-structures.md)

