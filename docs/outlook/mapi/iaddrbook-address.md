---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a13696b355e6fd815cd6bda42843505d9fc3d1f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579958"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно Outlook адресной книги. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Параметры

 _lpulUIParam_
  
> [in, out] Указатель на маркер родительского окна диалогового окна. На входе дескриптор окна всегда должен быть передан. На выходных данных Если член **ulFlags** для параметра _lpAdrParms_ установлено значение DIALOG_SDI, возвращаемый дескриптор окна безрежимным диалогового окна. См. раздел "Замечания". 
    
 _lpAdrParms_
  
> [in, out] Указатель на структуру [ADRPARM](adrparm.md) , определяющее представление и поведение диалоговое окно "адрес". 
    
 _lppAdrList_
  
> [in, out] Указатель на указатель на структуру [ADRLIST](adrlist.md) , содержащий сведения о получателях. На входные данные этот параметр может быть NULL или укажите допустимый указатель. В выходных данных этот параметр указывает указатель на допустимый адрес получателя. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Стандартным диалоговым окном адрес успешно отображается.
    
## <a name="remarks"></a>Замечания

Если элемент **ulFlags** параметр _lpAdrParms_ имеет значение DIALOG_SDI предупреждение return дескриптор окна безрежимным диалогового окна на выходных данных, он обрабатывается в Outlook; в отличные от Outlook всегда отображается версия модального диалогового окна. 
  
Структура **ADRLIST** , передается обратно по MAPI вызывающему через параметр _lppAdrList_ содержит массив структур [ADRENTRY](adrentry.md) одной структуры для каждого получателя. При передаче методу [IMessage::ModifyRecipients](imessage-modifyrecipients.md) исходящих сообщений с помощью параметра _lpMods_ структура **ADRLIST** можно использовать для обновление получателей списка. 
  
Структура каждого **ADRENTRY** в структуре **ADRLIST** содержит ноль или больше [SPropValue](spropvalue.md) структуры, структуры один для каждого свойства для получателя. При окно доклад **адрес** метод используется для удаления получателя может быть ноль **SPropValue** структуры. При наличии одного или нескольких структур **SPropValue** , соответствующий структура **ADRENTRY** используется для добавления или обновления получателя. Получатель может быть разрешен, это означает, что один из структур **SPropValue** описывает свойства получателя **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или разрешены, указывает, что свойство **PR_ENTRYID** отсутствует. 
  
В дополнение к **PR_ENTRYID**разрешить получателей относятся следующие свойства:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Структура **ADRLIST** , вызывающий объект передает в может быть другой размер структуры, которые возвращает MAPI. Если MAPI должен возвращать увеличенное структура **ADRLIST** , он освобождает исходной структуры и выделяет новый. После выделения памяти для структуры **ADRLIST** выделите память для каждой структуры **SPropValue** отдельно. Дополнительные сведения о том, как выделять и освобождать структуры **ADRLIST** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Адрес** возвращает немедленно, если флаг DIALOG_SDI установлен в член **ulFlags** структуры **ADRPARM** с помощью параметра _lpAdrParms_ . Флаг DIALOG_SDI игнорируется для клиентов, не являющиеся Outlook. Если DIALOG_SDI игнорируется, будет отображаться версия модального диалогового окна и указатель на маркер не следует ожидать в _lpulUIParam_.
  
 **Адрес** поддерживает строк символов Юникод в структуре **ADRPARM** , если в **ulFlags** членом **ADRPARM** с помощью параметра _lpAdrParms_ указано значение AB_UNICODEUI и поддерживает Юникод строк символов в ** ADRLIST**. Строки Юникод преобразуются в формат многобайтовой строки (MBCS), прежде чем они будут отображаться в диалоговом окне Outlook адресной книги.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |Mfcmapi (en) использует метод **адрес** разрешить пользователю выберите почтовый ящик, чтобы открыть.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

