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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна диалоговое окно, которое показано, если указано, чтобы побудить пользователя к устранению двусмысленности.
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют различные аспекты процесса разрешения. Можно установить следующие флаги:
    
AB_UNICODEUI
  
> Указывает, что  _lpszNewEntryTitle_ — это строка UNICODE. 
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен используйте только офлайн-адресную книгу. Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в кэшном режиме обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком Exchange адресной книги.
    
MAPI_DIALOG 
  
> Отображает диалоговое окно, чтобы подсказыть пользователю дополнительные сведения о разрешении имен. Если этот флаг не установлен, диалоговое окно не отображается. 
    
MAPI_UNICODE 
  
> Указывает, что свойства, возвращенные в списке адресов, должны иметь тип PT_UNICODE, а не PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Указатель на текст для заголовка управления в диалоговом окне, который побуждает пользователя ввести получателя. Название зависит от типа получателя. Параметр  _lpszNewEntryTitle_ может быть NULL. 
    
 _lpAdrList_
  
> [в выходе] Указатель на [структуру ADRLIST,](adrlist.md) которая содержит список разрешенных имен получателей. Эта **структура ADRLIST** может быть создана методом [IAddrBook::Address.](iaddrbook-address.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процесс разрешения имен удался.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> По крайней мере один получатель  _в параметре lpAdrList_ совпадает с несколькими входами в адресной книге. Обычно это значение возвращается при MAPI_DIALOG флага, запрещая отображение диалогового окна. 
    
MAPI_E_NOT_FOUND 
  
> Не удается разрешить по крайней мере одного получателя в _параметре lpAdrList._ Обычно это значение возвращается при MAPI_DIALOG флага, запрещая отображение диалогового окна. 
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг звонят по **методу ResolveName,** чтобы инициировать процесс разрешения имен. Неурегулированная запись — это запись, которая еще  не имеет идентификатора или PR_ENTRYID[(PidTagEntryId).](pidtagentryid-canonical-property.md)
  
 **ResolveName** проходит следующий процесс для каждой неурегулированной записи в списке адресов, переданных в _параметре lpAdrList._ 
  
1. Если тип адреса получателя придерживается формата SMTP-адреса _(имя_ @  _domain.top-level-domain),_ **ResolveName** назначает ему идентификатор одноуровневой записи. 
    
2. Для каждого контейнера **в свойстве PR_AB_SEARCH_PATH** [(PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md) **resolveName** вызывает [метод IABContainer::ResolveNames.](iabcontainer-resolvenames.md) **ResolveNames** пытается соответствовать отображаемого имени каждого неурегулированного получателя с отображаемым именем, которое принадлежит одной из его записей. 
    
3. Если контейнер не поддерживает **ResolveNames,** **ResolveName** ограничивает содержимое таблицы контейнера с помощью ограничения свойств **PR_ANR** [(PidTagAnr).](pidtaganr-canonical-property.md) Это ограничение приводит к выполнению контейнером поиска "наилучшего угадать", чтобы найти совпадающий получатель. Все контейнеры должны поддерживать ограничение **PR_ANR** свойств. 
    
4. Когда контейнер возвращает получателя, который соответствует нескольким именам, **ResolveName** отображает диалоговое окно, если MAPI_DIALOG флаг, который позволяет пользователю выбрать правильное имя. 
    
5. Если все контейнеры в  свойстве PR_AB_SEARCH_PATH были вызваны и не найдены совпадения, получатель остается неурегулированным. 
    
Если один или несколько получателей не разрешены, **ResolveName** возвращает MAPI_E_NOT_FOUND. Если у одного или более получателей было неоднозначное разрешение, которое не удалось разрешить диалоговым окном, или из-за того, что флаг MAPI_DIALOG не установлен, **ResolveName** возвращается MAPI_E_AMBIGUOUS_RECIP. Если некоторые из получателей неоднозначны, а некоторые не могут быть устранены, **ResolveName** может вернуть значение ошибки. 
  
Если имя не удается разрешить, клиент может создать разовый адрес, который имеет специально отформатированный адрес и идентификатор входа. Дополнительные сведения о формате идентификаторов одноавтной записи см. в документе [One-Off Entry Identifiers.](one-off-entry-identifiers.md) Дополнительные сведения о формате разных адресов см. в [одном из них.](one-off-addresses.md)
  
MAPI поддерживает строки символов Юникод для **ADRLIST** и новые параметры заголовка входа **в ResolveName;** Если задать флаг MAPI_UNICODE, следующие свойства возвращаются в виде PT_UNICODE в [структурах ADRENTRY:](adrentry.md) 
  
- **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
- **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
- **PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)
    
- **PR_TRANSMITABLE_DISPLAY_NAME** [(PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)
    
Однако свойство **PR_7BIT_DISPLAY_NAME** [(PidTag7BitDisplayName)](pidtag7bitdisplayname-canonical-property.md)всегда возвращается как тип PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**�����������**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI использует метод **ResolveName** для решения разового адреса перед добавлением его в сообщение.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI использует метод **ResolveName** для получения записи адресной книги по имени отображения.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

