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
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407909"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно адресной книги Outlook. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Параметры

 _lpulUIParam_
  
> [in, out] Указатель на окне родительского окна диалоговых окон. При вводе всегда должен передаваться окне окне. При выходе, если для члена **ulFlags**  _параметра lpAdrParms_ установлено DIALOG_SDI, возвращается окне окне диалоговых окон без режима. См. раздел "Замечания". 
    
 _lpAdrParms_
  
> [in, out] Указатель на [структуру ADRPARM,](adrparm.md) которая управляет представлением и поведением диалоговых окна адресов. 
    
 _lppAdrList_
  
> [in, out] Указатель на указатель на структуру [ADRLIST,](adrlist.md) которая содержит сведения о получателе. При вводе этот параметр может иметь NULL или указать допустимый указатель. В выходных данных этот параметр указывает на указатель на допустимые сведения о получателе. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Диалоговое окно общего адреса успешно отобразилось.
    
## <a name="remarks"></a>Примечания

Если для члена **ulFlags**  _параметра lpAdrParms_ задано DIALOG_SDI ожидание возврата окне окне в диалоговом окне без режима при выходе, он игнорируется в Outlook; Модальная версия диалогового окно всегда отображается в клиентах, не в том числе Outlook. 
  
Структура **ADRLIST,** переданная mapI вызываемой стороне с помощью параметра  _lppAdrList,_ содержит массив структур [ADRENTRY,](adrentry.md) по одной структуре для каждого получателя. При передании методу [IMessage::ModifyRecipients](imessage-modifyrecipients.md) исходяния сообщения в  _параметре lpMods_ структуру **ADRLIST** можно использовать для обновления списка получателей. 
  
Каждая **структура ADRENTRY** в структуре **ADRLIST** содержит ноль или несколько [структур SPropValue,](spropvalue.md) по одной структуре для каждого набора свойств получателя. Структуры **SPropValue** могут быть нулевой, если диалоговое окно, представляемые методом **Address,** используется для удаления получателя. Если имеется одна или несколько **структур SPropValue,** соответствующая **структура ADRENTRY** используется для добавления или обновления получателя. Получатель может быть разрешен, что означает, что одна из структур **SPropValue** описывает свойство **PR_ENTRYID** получателя [(PidTagEntryId)](pidtagentryid-canonical-property.md)или не разрешено, что указывает на то, что свойство **PR_ENTRYID** отсутствует. 
  
Помимо **PR_ENTRYID,** разрешенные получатели включают следующие свойства:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)
    
Структура **ADRLIST,** в которую передается звоняя, может быть отличается от структуры, возвращаемой MAPI. Если MAPI должен вернуть более крупную структуру **ADRLIST,** она освободит исходную структуру и выделит новую. При выделении памяти для **структуры ADRLIST** выделяете память для каждой **структуры SPropValue** отдельно. Дополнительные сведения о выделении и бесплатном выделении структур **ADRLIST** см. в под управлением памятью [для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Адрес** немедленно возвращается, DIALOG_SDI флага в члене **ulFlags** структуры **ADRPARM** в параметре _lpAdrParms._ Флаг DIALOG_SDI игнорируется для клиентов, не вехахав от Outlook. Если DIALOG_SDI игнорируется, отображается модальная версия диалоговое окно, и указатель на handle не следует ожидать в _lpulUIParam._
  
  Адрес поддерживает строки символов Юникода в структуре **ADRPARM,** если AB_UNICODEUI был указан в члене **ulFlags** **ADRPARM** в параметре _lpAdrParms_ и поддерживает строки символов Юникода в **ADRLIST.** Строки Юникода преобразуются в формат многобайтовых строк (MBCS) перед их отображением в диалоговом окне адресной книги Outlook.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI использует метод **Address,** чтобы позволить пользователю выбрать, какой почтовый ящик нужно открыть.  <br/> |
   
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

