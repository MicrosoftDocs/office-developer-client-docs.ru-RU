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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отображает общий диалоговое окно адресов. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameters

 _lpulUIParam_
  
> [in, out] Указатель на ручку родительского окна диалогового окна. При входе всегда должна быть передана ручка окна. При выходе флаг DIALOG_SDI в структуре [ADRPARM,](adrparm.md) на который указывает параметр  _lpAdrParms,_ возвращается ручка окна в диалоговом окне без режима. 
    
 _lpAdrParms_
  
> [in, out] Указатель на структуру **ADRPARM,** которая управляет презентацией и поведением диалоговое окно адресов. 
    
 _lppAdrList_
  
> [in, out] Указатель на указатель на список адресов. На входе этот список является текущим списком получателей в сообщении или NULL, если такого списка не существует. На выходе  _lppAdrList_ указывает на обновленный список получателей сообщений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Диалоговое окно адреса было успешно отображно.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::Address** реализован для объектов поддержки поставщика адресных книг. Поставщики адресных книг **звонят в Адрес,** чтобы создать или обновить список получателей сообщений. 
  
Каждый получатель описывается в структуре [ADRENTRY,](adrentry.md) которая входит в структуру [ADRLIST,](adrlist.md) на которую указывает параметр _lppAdrList._ Структура **ADRENTRY** содержит массив значений свойств получателей, одним из которых является тип получателя или **свойство PR_RECIPIENT_TYPE** [(PidTagRecipientType).](pidtagrecipienttype-canonical-property.md) Эта **структура ADRLIST** может быть передана клиенту для использования в качестве  _параметра lpMods_ в [вызове на IMessage::ModifyRecipients](imessage-modifyrecipients.md).
  
Каждый получатель в структуре **ADRLIST** может быть разрешен, что указывает на то, что одним из его свойств является свойство **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)или неурегулированное, что указывает на отсутствие PR_ENTRYID свойства.  
  
Помимо **PR_ENTRYID,** разрешенные получатели включают следующие свойства:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
- **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
- **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)
    
Неурегулированные получатели обычно включают **только PR_DISPLAY_NAME** и **PR_RECIPIENT_TYPE.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структура **ADRLIST,** в которую передается звонячий, может иметь другой размер от структуры, возвращаемой MAPI. При выделении памяти для **структуры ADRLIST** выделяем память для каждой [структуры SPropValue](spropvalue.md) отдельно. 
  
Для выделения памяти используйте указатели для функций распределения памяти MAPI, переданных в функцию [ABProviderInit.](abproviderinit.md) Распределите память функцией [MAPIAllocateBuffer](mapiallocatebuffer.md) для **ADRLIST** и каждой структурой значений свойств в структурах **ADRENTRY** в **ADRLIST.** 
  
Если **адрес** должен возвращать более крупную структуру **ADRLIST** или если вы прошли  NULL для _lppAdrList,_ адрес освободит исходную структуру и выделит новую. **Адрес** также выделяет дополнительные структуры значений свойств в **структуре ADRLIST** и по мере необходимости освободит старые. Дополнительные сведения о том, как управлять памятью для **структур ADRLIST,** см. в рубрике Управление памятью для [структур ADRLIST и SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Адрес** возвращается немедленно, если DIALOG_SDI флаг был задан в структуре **ADRPARM** в параметре _lpAdrParms._ 
  
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

