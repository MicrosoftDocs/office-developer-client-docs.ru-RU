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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно Outlook адресной книги. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameters

 _lpulUIParam_
  
> [in, out] Указатель на ручку родительского окна диалогового окна. При входе всегда должна быть передана ручка окна. На выходе, если для члена **ulFlags**  _параметра lpAdrParms_ установлено DIALOG_SDI, возвращается ручка окна в диалоговом окне без режима. См. раздел "Замечания". 
    
 _lpAdrParms_
  
> [in, out] Указатель на структуру [ADRPARM,](adrparm.md) которая управляет презентацией и поведением диалоговое окно адресов. 
    
 _lppAdrList_
  
> [in, out] Указатель на указатель на структуру [ADRLIST,](adrlist.md) которая содержит сведения о получателе. При вводе этот параметр может быть NULL или указать допустимый указатель. На выходе этот параметр указывает на указатель на допустимые данные получателя. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Общий диалоговое окно адресов было успешно отображёно.
    
## <a name="remarks"></a>Примечания

Если для **участника ulFlags** _параметра lpAdrParms_ установлено DIALOG_SDI, предвидя возвращение ручки окна в режимном диалоговом окне на выходе, он игнорируется в Outlook; модальная версия диалоговое окно всегда отображается в Outlook клиентах. 
  
Структура **ADRLIST,** переданная MAPI вызываемой стороне через параметр  _lppAdrList,_ содержит массив структур [ADRENTRY,](adrentry.md) по одной структуре для каждого получателя. При переходе к методу [IMessage::ModifyRecipients](imessage-modifyrecipients.md) в параметре  _lpMods_ структура **ADRLIST** может использоваться для обновления списка получателей. 
  
Каждая **структура ADRENTRY** в структуре **ADRLIST** содержит нулевые или более [структур SPropValue,](spropvalue.md) по одной структуре для каждого свойства, задаваемой получателю. Структуры **SPropValue** могут быть нулевыми, если диалоговое окно, представленного методом **Address,** используется для удаления получателя. Если существует одна или несколько **структур SPropValue,** для добавления или обновления получателя используется соответствующая структура **ADRENTRY.** Получатель может быть разрешен, что указывает на то, что одна из структур  **SPropValue** описывает свойство **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)или неурегулированное, что указывает на отсутствие PR_ENTRYID свойства. 
  
Помимо **PR_ENTRYID,** разрешенные получатели включают следующие свойства:
  
- **PR_RECIPIENT_TYPE** [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)
    
- **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
- **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
- **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)
    
Структура **ADRLIST,** в которую передается звонячий, может иметь другой размер от структуры, возвращаемой MAPI. Если MAPI должен вернуть более крупную **структуру ADRLIST,** она освободит исходную структуру и выделит новую. При выделении памяти для **структуры ADRLIST** выделяем память для каждой **структуры SPropValue** отдельно. Дополнительные сведения о выделении и бесплатном выделении структур **ADRLIST** см. в рубрике Управление памятью [для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Адрес** возвращается немедленно, если DIALOG_SDI флаг установлен в члене **ulFlags** структуры **ADRPARM** в параметре _lpAdrParms._ Флаг DIALOG_SDI игнорируется для клиентов, не Outlook клиентов. Если DIALOG_SDI игнорируется, будет отображаться модальная версия диалоговое окно, а указатель на ручку не следует ожидать в  _lpulUIParam_.
  
  Адрес поддерживает строки символов Юникод в структуре **ADRPARM,** если AB_UNICODEUI был указан в члене **ulFlags** **ADRPARM** в параметре _lpAdrParms,_ и поддерживает строки символов Юникод в **ADRLIST**. Строки Юникода преобразуются в формат многобайтной строки символов (MBCS) перед их отображением в диалоговом окне Outlook адресной книги.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI использует метод **Address,** чтобы позволить пользователю выбрать открытый почтовый ящик.  <br/> |
   
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

