---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408133"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которые контролируют различные аспекты процесса разрешения. Можно установить следующие флаги:
    
AB_UNICODEUI
  
> Указывает,  _что lpszNewEntryTitle_ является строкой ЮНИКОДА. 
    
MAPI_CACHE_ONLY
  
> Используйте только автономной адресной книги для разрешения имен. Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком адресной книги Exchange.
    
MAPI_DIALOG 
  
> Отображает диалоговое окно с запросом дополнительных сведений о разрешении имен. Если этот флаг не установлен, диалоговое окно не отображается. 
    
MAPI_UNICODE 
  
> Указывает, что возвращаемая в списке адресов информация о свойствах должна иметь тип PT_UNICODE, а не PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Указатель на текст для заголовка управления в диалоговом окне с запросом ввода получателя. Заголовок зависит от типа получателя. Параметр  _lpszNewEntryTitle_ может иметь NULL. 
    
 _lpAdrList_
  
> [in-out] Указатель на [структуру ADRLIST,](adrlist.md) которая содержит список имен получателей, которые необходимо разрешить. Эту **структуру ADRLIST** можно создать с помощью метода [IAddrBook::Address.](iaddrbook-address.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процесс разрешения имен был успешно успешным.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> По крайней мере один получатель в параметре  _lpAdrList_ соответствует нескольким записям в адресной книге. Обычно это значение возвращается при MAPI_DIALOG флага, запрещая отображение диалоговых окно. 
    
MAPI_E_NOT_FOUND 
  
> Не удается разрешить хотя бы одного получателя в параметре _lpAdrList._ Обычно это значение возвращается при MAPI_DIALOG флага, запрещая отображение диалоговых окно. 
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг **звонят методу ResolveName,** чтобы инициировать процесс разрешения имен. Не разрешенная запись — это запись, у нее еще нет идентификатора записи **или** PR_ENTRYID ([PidTagEntryId).](pidtagentryid-canonical-property.md)
  
 **ResolveName** проходит следующий процесс для каждой не разрешенной записи в списке адресов, переданной в _параметре lpAdrList._ 
  
1. Если тип адреса получателя соответствует формату SMTP-адреса  @  _(displayname domain.top-level-domain),_ **ResolveName** назначает ему одноуровневый идентификатор записи. 
    
2. Для каждого контейнера **в свойстве PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) **ResolveName** вызывает метод [IABContainer::ResolveNames.](iabcontainer-resolvenames.md) **ResolveNames** пытается найти отображаемую имя каждого неу разрешенного получателя с отображаемым именем, которое принадлежит одной из записей. 
    
3. Если контейнер не поддерживает **ResolveNames,** **ResolveName** ограничивает таблицу содержимого контейнера с помощью ограничения свойства **PR_ANR** ([PidTagAnr).](pidtaganr-canonical-property.md) Это ограничение приводит к выполнению контейнером "наилучшего угадать" типа поиска, чтобы найти нужного получателя. Все контейнеры должны поддерживать ограничение **PR_ANR** свойств. 
    
4. Когда контейнер возвращает получателя, который соответствует нескольким именам, **ResolveName** отображает диалоговое окно, если установлен флаг MAPI_DIALOG, что позволяет пользователю выбрать правильное имя. 
    
5. Если все контейнеры в  свойстве PR_AB_SEARCH_PATH были вызваны и совпадение не найдено, получатель остается не разрешенным. 
    
Если один или несколько получателей не разрешены, **ResolveName** возвращает MAPI_E_NOT_FOUND. Если у одного или более получателей было неоднозначное разрешение, которое не удалось разрешить с помощью диалоговых окне или из-за того, что флаг MAPI_DIALOG не установлен, **ResolveName** возвращает MAPI_E_AMBIGUOUS_RECIP. Если некоторые получатели неоднозначны, а некоторые не могут быть разрешены, **ResolveName** может вернуть значение ошибки. 
  
Если имя не может быть разрешено, клиент может создать разовый адрес, который имеет специально отформатированный адрес и идентификатор записи. Дополнительные сведения о формате идентификаторов одноаваторной записи см. в документе [One-Off Entry Identifiers.](one-off-entry-identifiers.md) Дополнительные сведения о формате разных адресов см. в этой [теме.](one-off-addresses.md)
  
MAPI поддерживает строки символов Юникода для **ADRLIST** и новые параметры заголовка записи **для ResolveName;** Если вы установите флаг MAPI_UNICODE, следующие свойства возвращаются как тип PT_UNICODE в структурах [ADRENTRY:](adrentry.md) 
  
- **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)
    
Однако свойство **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName)](pidtag7bitdisplayname-canonical-property.md)всегда возвращается как тип PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**�����������**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI использует метод **ResolveName** для разрешения одноразового адреса перед его добавлением в сообщение.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI использует метод **ResolveName** для получения записи адресной книги по отображаемого имени.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

