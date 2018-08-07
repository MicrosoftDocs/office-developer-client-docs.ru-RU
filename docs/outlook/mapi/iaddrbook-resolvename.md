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
ms.openlocfilehash: aa72085c4e50fcef1f2d3da81e5409af3d55d89b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808753"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Относится к**: Outlook 
  
Выполняет разрешение имен, назначение идентификаторов запись для получателей в список получателей.
  
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
  
> [in] Дескриптор родительского окна диалоговое окно, которое отображается, если указано, чтобы запрашивать у пользователя разрешение неопределенность.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющие различных аспектов процесса разрешения. Можно задать следующие флажки:
    
AB_UNICODEUI
  
> Указывает, что этот _lpszNewEntryTitle_ — это строка Юникод. 
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен используйте автономной адресной книги. Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения. Этот флаг поддерживается только поставщик Exchange адресной книги.
    
MAPI_DIALOG 
  
> Отображает диалоговое окно запрашивать у пользователя для сведений о разрешении дополнительных имен. Если этот флаг не установлен, диалоговое окно не отображается. 
    
MAPI_UNICODE 
  
> Указывает, что возвращаемые в списке адресов свойства должны быть в формате PT_UNICODE вместо PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Указатель на текст в поле заголовок элемента управления в диалоговом окне запрос на ввод получателя. Заголовок может отличаться в зависимости от типа получателя. Параметр _lpszNewEntryTitle_ может быть NULL. 
    
 _lpAdrList_
  
> [входной-выходной параметр] Указатель на структуру [ADRLIST](adrlist.md) , содержащего список получателей разрешения имен. Эта структура **ADRLIST** могут создаваться с помощью метода [IAddrBook::Address](iaddrbook-address.md) . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Процесс разрешения имен выполнено успешно.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> По крайней мере один получатель с помощью параметра _lpAdrList_ сопоставлен более одной операции в адресной книге. Как правило это значение возвращается, если флаг MAPI_DIALOG установлен, Запрет отображения диалогового окна. 
    
MAPI_E_NOT_FOUND 
  
> Не удалось разрешить по крайней мере один получатель с помощью параметра _lpAdrList_ . Как правило это значение возвращается, если флаг MAPI_DIALOG установлен, Запрет отображения диалогового окна. 
    
## <a name="remarks"></a>Замечания

Клиенты и поставщики услуг вызовите метод **ResolveName** начать процесс разрешения имен. Нерешенные запись является записью, которая не имеет идентификатор записи или свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **ResolveName** проходит через процесс для каждой нерешенные записи в списке адресов, переданной в параметре _lpAdrList_ . 
  
1. Если тип адреса получателя, соответствующий формат SMTP-адреса ( _displayname_@ _domain.top уровень домена_), **ResolveName** назначается идентификатор единичных записей. 
    
2. Для каждого контейнера в свойстве **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) **ResolveName** вызывается метод [IABContainer::ResolveNames](iabcontainer-resolvenames.md) . **ResolveNames** пытается сопоставить отображаемое имя каждого получателя, нерешенные с отображаемым именем, к которому относится к одному из его записи. 
    
3. Если контейнер не поддерживает **ResolveNames**, **ResolveName** ограничивает контейнера содержимого таблицы с помощью ограничение свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Это ограничение вызывает контейнер для выполнения типа «лучше всего подбора» поиск, чтобы найти получатель. Все контейнеры должны поддерживать ограничение свойства **PR_ANR** . 
    
4. При возвращении получателя, который соответствует несколько имен контейнером **ResolveName** отображает диалоговое окно, если установлен флаг MAPI_DIALOG, позволяющее пользователю выбрать правильное имя. 
    
5. Если все контейнеров в свойстве **PR_AB_SEARCH_PATH** вызван и не найдено, получатель не устранена. 
    
Если один или несколько получателей разрешены, **ResolveName** возвращает MAPI_E_NOT_FOUND. Если неоднозначные решение, которое не удалось разрешить диалоговое окно с одного или нескольких получателей, или не был установлен флажок MAPI_DIALOG, **ResolveName** возвращает MAPI_E_AMBIGUOUS_RECIP. Когда некоторых получателей неоднозначным и некоторые не может быть разрешен, **ResolveName** может вернуть либо значение ошибки. 
  
Если не удается разрешить имя, клиента можно создать указывает адрес, который имеет специально созданный адрес и идентификатор записи. Дополнительные сведения о формате идентификаторов единичных записей можно [Одноразовых идентификаторы записей](one-off-entry-identifiers.md). Дополнительные сведения о формате одноразовых адресов можно [Одноразовых адреса](one-off-addresses.md).
  
MAPI поддерживает знаков Юникод для **ADRLIST** и новых параметров заголовка входа **ResolveName**; Если значение флага MAPI_UNICODE, в качестве типа PT_UNICODE структур [ADRENTRY](adrentry.md) возвращаются следующие свойства: 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Свойство **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) всегда возвращается как тип PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |Mfcmapi (en) использует метод **ResolveName** обрабатывать указывает адрес до его добавления к сообщению.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |Mfcmapi (en) использует метод **ResolveName** для поиска запись книги по отображаемому имени.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

