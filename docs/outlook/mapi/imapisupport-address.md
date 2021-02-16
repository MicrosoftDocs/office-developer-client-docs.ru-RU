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
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407321"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно общего адреса. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Параметры

 _lpulUIParam_
  
> [in, out] Указатель на ладку родительского окна диалоговых окон. При вводе всегда должен передаваться окне окне. Если флаг DIALOG_SDI установлен в структуре [ADRPARM,](adrparm.md) на который указывает параметр  _lpAdrParms,_ возвращается окне окне в диалоговом окне без режима. 
    
 _lpAdrParms_
  
> [in, out] Указатель на **структуру ADRPARM,** которая управляет представлением и поведением диалоговых окна адресов. 
    
 _lppAdrList_
  
> [in, out] Указатель на указатель на список адресов. При вводе этот список является текущим списком получателей в сообщении или NULL, если такого списка нет. При выходе  _lppAdrList_ указывает на обновленный список получателей сообщений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Диалоговое окно адреса успешно отобразилось.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::Address** реализован для объектов поддержки поставщика адресной книги. Поставщики адресных книг **звонят** по адресу, чтобы создать или обновить список получателей сообщений. 
  
Каждый получатель описывается в структуре [ADRENTRY,](adrentry.md) включенной в структуру [ADRLIST,](adrlist.md) на которую указывает параметр _lppAdrList._ Структура **ADRENTRY** содержит массив значений свойств получателя, одно из которых является типом получателя или **свойством PR_RECIPIENT_TYPE** ([PidTagRecipientType).](pidtagrecipienttype-canonical-property.md) Эта **структура ADRLIST** может быть передана клиенту для использования в качестве параметра  _lpMods_ в вызове [IMessage::ModifyRecipients](imessage-modifyrecipients.md).
  
Каждый получатель в структуре **ADRLIST** может быть разрешен, что означает, что одно из его значений свойства — это его **свойство PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)или не разрешено, что указывает на то, что свойство **PR_ENTRYID** отсутствует. 
  
Помимо **PR_ENTRYID,** разрешенные получатели включают следующие свойства:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
- **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)
    
Как правило, не разрешенные получатели включают **только** PR_DISPLAY_NAME и **PR_RECIPIENT_TYPE.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структура **ADRLIST,** в которую передается звоняя, может быть отличается от структуры, возвращаемой MAPI. При выделении памяти для **структуры ADRLIST** выделяете память для каждой [структуры SPropValue](spropvalue.md) отдельно. 
  
Используйте указатели на функции выделения памяти MAPI, переданные функции [ABProviderInit](abproviderinit.md) для выделения памяти. Выделите память с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) для **ADRLIST** и каждой структуры значений свойств в структурах **ADRENTRY** **в ADRLIST.** 
  
Если **адрес** должен возвращать более крупную структуру **ADRLIST** или если вы передали NULL для _lppAdrList,_ address освободит исходную структуру и выделит новую.  **Адрес** также выделяет дополнительные структуры значений свойств в структуре **ADRLIST** и при необходимости освободит старые. Дополнительные сведения об управлении памятью для структур **ADRLIST** см. в под управлением памятью [для ADRLIST и структур SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Адрес** немедленно возвращается, DIALOG_SDI флага, установленного в структуре **ADRPARM** в параметре _lpAdrParms._ 
  
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

