---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405102"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет нового получателя в контейнер адресной книги или в список получателей исходя из сообщения.
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна для диалоговое окно.
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом используемого текста. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _cbEIDContainer_
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpEIDContainer._ 
    
 _lpEIDContainer_
  
> [in] Указатель на идентификатор входа контейнера, в котором должен быть добавлен новый получатель. Если параметр _cbEIDContainer_ нулевой, метод **NewEntry** возвращает идентификатор входа получателя и список шаблонов, как если бы был вызван метод [IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md) 
    
 _cbEIDNewEntryTpl_
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpEIDNewEntryTpl._ 
    
 _lpEIDNewEntryTpl_
  
> [in] Указатель на разовую шаблон, которая будет использоваться для создания нового получателя. Если  _cbEIDNewEntryTpl_ ноль, а  _lpEIDNewEntryTpl_ — NULL, **NewEntry** отображает диалоговое окно, с помощью которого пользователь может выбрать из списка шаблонов для добавления новых записей. 
    
 _lpcbEIDNewEntry_
  
> [вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEIDNewEntry._ 
    
 _lppEIDNewEntry_
  
> [вышел] Указатель на указатель на идентификатор записи нового получателя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новая запись адресной книги была успешно создана.
    
## <a name="remarks"></a>Примечания

Метод **NewEntry** создает новую запись адресной книги, которая должна быть добавлена непосредственно в контейнер или использоваться для решения исходяющих сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вы хотите, чтобы новая запись была добавлена в определенный контейнер, установите  _lpEIDContainer_ в идентификатор входа контейнера и  _cbEIDContainer_ к счету byte в идентификаторе записи. 
  
Если вы хотите, чтобы новая запись была добавлена в список получателей исходячего сообщения, установите  _значение lpEIDContainer_ nULL и  _cbEIDContainer_ до нуля. 
  
Если вы хотите разрешить пользователю клиентского приложения выбрать тип создаваемой записи, сдайте ноль в  _cbEIDNewEntryTpl_ и NULL в  _lpEIDNewEntryTpl_. Метод **NewEntry** отображает разовую таблицу MAPI, список шаблонов, поддерживаемых MAPI и каждым поставщиком адресных книг в сеансе. Каждый шаблон может создать запись получателя для одного или более типов адресов. 
  
Если вы хотите сохранить идентификатор входа новой записи, передай допустимые указатели в параметрах _lpcbEIDNewEntry_ и _lppEIDNewEntry._ Вы несете ответственность за то, чтобы освободить этот идентификатор записи после его завершения, позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Чтобы использовать определенный шаблон для добавления новой записи в модификабельный контейнер, используйте следующую процедуру:
  
1. Вызов [метода IMAPISession::OpenEntry](imapisession-openentry.md) для открытия контейнера назначения и установите параметр  _lpEntryID_ в идентификатор входа контейнера. 
    
2. Вызов метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера назначения **и** установите параметр _ulPropTag_ PR_CREATE_TEMPLATES [(PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)и параметр _lpiid_ для IID_IMAPITable. Контейнер возвращает разовую таблицу, в которую перечислены все шаблоны, которые он поддерживает для создания новых записей. 
    
3. Извлечение строки, которая представляет шаблон для определенного типа записи, которую вы хотите создать. Столбец **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)указывает тип адреса, поддерживаемый шаблоном.
    
4. Вызов метода **NewEntry** и установите  _lpEIDNewEntryTpl_ в идентификатор входа выбранного шаблона. Идентификатором записи будет **столбец PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)из строки шаблона в разовой таблице. Pass zero в  _cbEIDContainer_ и NULL в  _lpEIDContainer_. Передай допустимый указатель в  _параметре lppEIDNewEntry,_ если вы хотите сохранить идентификатор записи новой записи. 
    
## <a name="see-also"></a>См. также



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

