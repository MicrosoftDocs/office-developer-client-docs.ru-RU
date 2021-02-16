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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Добавляет нового получателя в контейнер адресной книги или в список получателей исходяного сообщения.
  
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

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window for the dialog box.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом используемого текста. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _cbEIDContainer_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEIDContainer._ 
    
 _lpEIDContainer_
  
> [in] Указатель на идентификатор записи контейнера, в который будет добавлен новый получатель. Если параметр _cbEIDContainer_ имеет нулевое значение, метод **NewEntry** возвращает идентификатор записи получателя и список шаблонов, как если бы был вызван метод [IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md) 
    
 _cbEIDNewEntryTpl_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEIDNewEntryTpl._ 
    
 _lpEIDNewEntryTpl_
  
> [in] Указатель на разротной шаблон, который будет использоваться для создания нового получателя. Если  _cbEIDNewEntryTpl_ имеет нулевое значение, а  _lpEIDNewEntryTpl_ — NULL, **NewEntry** отображает диалоговое окно, в котором пользователь может выбрать из списка шаблонов для добавления новых записей. 
    
 _lpcbEIDNewEntry_
  
> [out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppEIDNewEntry._ 
    
 _lppEIDNewEntry_
  
> [out] Указатель на указатель на идентификатор записи нового получателя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новая запись адресной книги успешно создана.
    
## <a name="remarks"></a>Примечания

Метод **NewEntry** создает новую запись адресной книги, которая добавляется непосредственно в контейнер или используется для обращения к исходя новому сообщению. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вы хотите добавить новую запись в определенный контейнер, задайте  _для lpEIDContainer_ идентификатор записи контейнера, а  _для cbEIDContainer_ количество в идентификаторе записи. 
  
Если вы хотите добавить новую запись в список получателей исходячего сообщения, установите для  _lpEIDContainer_ значение NULL, а  _для cbEIDContainer_ значение n. 
  
Если вы хотите разрешить пользователю клиентского приложения выбирать тип создаемой записи, передайте ноль  _в cbEIDNewEntryTpl_ и NULL в  _lpEIDNewEntryTpl_. Метод **NewEntry** отображает одностолевую таблицу MAPI, список шаблонов, поддерживаемых MAPI и каждым поставщиком адресной книги в сеансе. Каждый шаблон может создать запись получателя для одного или более типов адресов. 
  
Если вы хотите сохранить идентификатор записи новой записи, передав допустимые указатели в параметрах _lpcbEIDNewEntry_ и _lppEIDNewEntry._ Вы несете ответственность за то, чтобы освободить этот идентификатор записи после завершения работы с ним путем вызова функции [MAPIFreeBuffer.](mapifreebuffer.md) 
  
Чтобы использовать определенный шаблон для добавления новой записи в измояемый контейнер, используйте следующую процедуру:
  
1. Вызовите метод [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы открыть контейнер назначения, и установите для параметра  _lpEntryID_ идентификатор записи контейнера. 
    
2. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера назначения и установите для параметра  _ulPropTag_ PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates),](pidtagcreatetemplates-canonical-property.md)а для параметра  _lpiid_ — IID_IMAPITable. Контейнер возвращает одностолевую таблицу со списком всех шаблонов, которые он поддерживает для создания новых записей. 
    
3. Извлекает строку, представляюную шаблон для определенного типа записи, которую необходимо создать. Столбец **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)указывает тип адреса, поддерживаемый шаблоном.
    
4. Вызовите **метод NewEntry** и установите  _для lpEIDNewEntryTpl_ идентификатор записи выбранного шаблона. Идентификатором записи будет **столбец PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)из строки шаблона в одноразовой таблице. Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_. Передав допустимый указатель в  _параметре lppEIDNewEntry,_ если необходимо сохранить идентификатор записи новой записи. 
    
## <a name="see-also"></a>См. также



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

