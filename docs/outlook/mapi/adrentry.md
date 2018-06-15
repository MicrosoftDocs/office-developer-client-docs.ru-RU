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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 4b6f850c8f88088863b37bd94de6b1f3d4c48d4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808046"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Применимо к**: Outlook 
  
Описание ноль или больше свойств, относящихся к получателя.
  
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

## <a name="members"></a>Элементы

 **ulReserved1**
  
> Зарезервировано; должно быть равно нулю.
    
 **cValues**
  
> Число свойств в массиве значение свойства, на который указывает член **rgPropVals** . Член **cValues** может быть равно нулю. 
    
 **rgPropVals**
  
> Указатель на массив значений свойства, описывающие свойства для получателя. Элемент **rgPropVals** может быть NULL. 
    
## <a name="remarks"></a>Замечания

Структура с **ADRENTRY** описание свойств, относящихся к одного получателя. Следующие свойства, которые обычно используются для описания получателя. 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Если идентификатор записи или свойство **PR_ENTRYID** появится в массиве [SPropValue](spropvalue.md) для получателя, это значит, что получатель была устранена. Клиенты вызовите метод [IAddrBook::ResolveName](iaddrbook-resolvename.md) для убедитесь в том, что всех получателей в списке получателей исходящих сообщений, устранены. Только разрешения получателей можно отправить с сообщениями. 
  
 **ADRENTRY** структуры обычно объединяются для создания массива для элемента **aEntries** структуры [ADRLIST](adrlist.md) . 
  
 **ADRENTRY** структуры и структуры [SRow](srow.md) идентичны, так как они содержали зарезервированного элемента, массив значений свойств и количество значений в массиве. В то время как структуры **ADRENTRY** объединяются для создания члена **aEntries** структуры **ADRLIST** , **SRow** структуры объединяются для создания члена **aRow** структуры [SRowSet](srowset.md) . Обоих типов структур следуйте этим правилам для распределения, подразумевает, что структуру **SRowSet** , полученной из таблицы содержимого контейнера адресной книги может привести к структуре **ADRLIST** и использовать. 
  
Структура с **ADRENTRY** может быть пустым. Например структуру **ADRENTRY** , содержащихся в структуре **ADRLIST** указывает параметр _lppAdrList_ в вызове **IAddrBook::Address** может быть пустым при удалении получателя. 
  
Дополнительные сведения о том, как выделить память для структуры **ADRENTRY** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>См. также



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Структуры MAPI](mapi-structures.md)

