---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 524bbfe5f40a66585fb4ed4463b057ca6a0c881a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586804"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно Общие адреса. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Параметры

 _lpulUIParam_
  
> [in, out] Указатель на дескриптор окна родительского диалогового окна. На входе дескриптор окна всегда должен быть передан. В выходных данных Если в структуре [ADRPARM](adrparm.md) , на который указывает параметр _lpAdrParms_ установлен флаг DIALOG_SDI возвращается дескриптор окна безрежимным диалогового окна. 
    
 _lpAdrParms_
  
> [in, out] Указатель на структуру **ADRPARM** , определяющее представление и поведение диалоговое окно "адрес". 
    
 _lppAdrList_
  
> [in, out] Указатель на указатель на список адресов. Для ввода данных этот список является либо текущий список получателей в сообщении или значение NULL, если список не существует. На выходе _lppAdrList_ указывает на обновленный список получателей сообщения. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Диалоговое окно "адрес" успешно отображается.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::Address** реализуется для объектов поддержки поставщик адресной книги. Поставщиками адресной книги вызовите **адрес** , который необходимо создать или обновить список получателей сообщения. 
  
Каждого получателя, описанного в структуре [ADRENTRY](adrentry.md) , включенную в структуре [ADRLIST](adrlist.md) указывает параметр _lppAdrList_ . Структура **ADRENTRY** содержит массив значений свойства получателей, один из которых является тип получателя или свойство **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Эта структура **ADRLIST** может быть передан клиента для использования в качестве параметра _lpMods_ в вызове [IMessage::ModifyRecipients](imessage-modifyrecipients.md).
  
Каждого получателя в структуре **ADRLIST** может быть либо разрешен, это означает, что одно из значений его свойств, его свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), или разрешены, указывает, что свойство **PR_ENTRYID** отсутствует. 
  
В дополнение к **PR_ENTRYID**разрешить получателей относятся следующие свойства:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Нерешенные получателей относятся только **PR_DISPLAY_NAME** и **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структура **ADRLIST** , вызывающий объект передает в может быть другой размер структуры, которые возвращает MAPI. После выделения памяти для структуры **ADRLIST** выделите память для каждой структуры [SPropValue](spropvalue.md) отдельно. 
  
Используйте указатели на функции выделения памяти MAPI, переданных в функции [ABProviderInit](abproviderinit.md) для выделения памяти. Выделите память с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) для **ADRLIST** и структуры значение каждого свойства в структур **ADRENTRY** в **ADRLIST**. 
  
Если **адрес** должен вернуть увеличенное структуру **ADRLIST** или переданное значение NULL для _lppAdrList_, **адрес** освобождает исходной структуры и выделяет новый. **Адрес** также выделяет структур значение дополнительные свойства в структуре **ADRLIST** и освобождает старых соответствующим образом. Дополнительные сведения об управлении памяти **ADRLIST** структуры можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Адрес** возвращает немедленно, если был установлен флажок DIALOG_SDI в структуре **ADRPARM** в параметре _lpAdrParms_ . 
  
## <a name="see-also"></a>См. также



[ABProviderInit](abproviderinit.md)
  
[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagAddressType](pidtagaddresstype-canonical-property.md)
  
[Каноническое свойство PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Каноническое свойство PidTagDisplayType](pidtagdisplaytype-canonical-property.md)
  
[Каноническое свойство PidTagEntryId](pidtagentryid-canonical-property.md)
  
[Каноническое свойство PidTagRecipientType](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

