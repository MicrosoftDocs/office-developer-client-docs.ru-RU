---
title: имаписуппортаддресс
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
  
Отображает диалоговое окно "общий адрес". 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Параметры

 _лпулуипарам_
  
> [вход, выход] Указатель на дескриптор родительского окна диалогового окна. Во входных данных дескриптор окна всегда должен быть передан. В выходных данных, если флаг DIALOG_SDI задается в структуре [адрпарм](adrparm.md) , на которую указывает параметр _лпадрпармс_ , возвращается дескриптор окна немодального диалогового окна. 
    
 _лпадрпармс_
  
> [вход, выход] Указатель на структуру **адрпарм** , которая управляет представлением и поведением диалогового окна "адрес". 
    
 _лппадрлист_
  
> [вход, выход] Указатель на указатель на список адресов. При вводе этот список является либо текущим списком получателей в сообщении, либо значением NULL, если такого списка не существует. В выходных данных _лппадрлист_ указывает на обновленный список получателей сообщения. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Диалоговое окно "адрес" успешно отображено.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: Address** реализован для объектов поддержки поставщика адресных книг. Поставщик адресных книг **адрес** вызова для создания или обновления списка получателей сообщения. 
  
Каждый получатель описан в структуре [адрентри](adrentry.md) , которая включается в структуру [ADRLIST](adrlist.md) , на которую указывает параметр _лппадрлист_ . Структура **адрентри** содержит массив значений свойств Recipient, один из которых является типом получателя или свойство **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Эту структуру **ADRLIST** можно передать клиенту, чтобы использовать в качестве параметра _лпмодс_ в вызове [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md).
  
Каждый получатель в структуре **ADRLIST** может быть разрешаемым, что указывает на то, что одно из значений свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или не определено, что указывает на отсутствие свойства **PR_ENTRYID** . 
  
Кроме **PR_ENTRYID**, разрешенные получатели включают следующие свойства:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Как правило, нераспознанным получателям относятся только **PR_DISPLAY_NAME** и **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структура **ADRLIST** , которую передает вызывающий абонент, может иметь другой размер из структуры, которую возвращает MAPI. При выделении памяти для структуры **ADRLIST** выделяет память для каждой структуры [спропвалуе](spropvalue.md) отдельно. 
  
Используйте указатели на функции выделения памяти MAPI, передаваемые функции [абпровидеринит](abproviderinit.md) для выделения памяти. Выделение памяти с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) для **ADRLIST** и каждой структуры значений свойств в структурах **адрентри** в **ADRLIST**. 
  
Если **Address** должен возвращать более крупную структуру **ADRLIST** , или если для _лппадрлист_было передано значение null, то **Address** освобождает исходную структуру и выделяет новую. **Address** также выделяет дополнительные структуры значений свойств в структуре **ADRLIST** и освобождает старые, если это необходимо. Дополнительные сведения об управлении памятью для структур **ADRLIST** приведены в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Адрес** немедленно возвращается, если установлен флаг DIALOG_SDI в структуре **адрпарм** в параметре _лпадрпармс_ . 
  
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

