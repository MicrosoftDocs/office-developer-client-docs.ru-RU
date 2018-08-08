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
ms.openlocfilehash: e9b9ae316749659c6fc6a043bfb72c49010ccc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808774"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Относится к**: Outlook 
  
Добавляет нового получателя контейнер адресной книги или списка получателей исходящих сообщений.
  
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
  
> [in] Дескриптор родительского окна для диалогового окна.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип текст, который используется. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _cbEIDContainer_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [in] Указатель на идентификатор записи контейнер, в котором для добавления нового получателя. Если параметр _cbEIDContainer_ равно нулю, метод **NewEntry** возвращает идентификатор получателя записи и список шаблонов, как если бы метод [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) вызван. 
    
 _cbEIDNewEntryTpl_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [in] Указатель на одноразовых шаблон, который будет использоваться для создания нового получателя. Если _cbEIDNewEntryTpl_ равно нулю, а _lpEIDNewEntryTpl_ имеет значение NULL, **NewEntry** отображает диалоговое окно, с помощью которой пользователь может выбрать из списка шаблонов для добавления новых записей. 
    
 _lpcbEIDNewEntry_
  
> [out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Указатель на указатель на идентификатор записи нового получателя.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Новые записи адресной книги был успешно создан.
    
## <a name="remarks"></a>Замечания

Метод **NewEntry** создает новую запись книги адреса, добавляемого непосредственно в контейнер или для использования с учетом исходящих сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Новая запись будет добавлена к конкретному контейнеру, установите _lpEIDContainer_ идентификатор записи и _cbEIDContainer_ на число байтов в идентификатор записи контейнера. 
  
Новая запись будет добавлена в список получателей исходящих сообщений, установите _lpEIDContainer_ NULL и _cbEIDContainer_ присваивается значение 0. 
  
Если вы хотите разрешить пользователю создавать клиентского приложения, чтобы выбрать тип записи, передайте ноль в _cbEIDNewEntryTpl_ и NULL в _lpEIDNewEntryTpl_. Метод **NewEntry** отображаются в таблице одноразовых MAPI, список шаблонов, MAPI и каждый поставщик адресной книги поддерживают в сеансе. В каждый шаблон можно создать запись получателей для одного или нескольких типов адресов. 
  
Если вы хотите сохранить идентификатор записи новой записи, передайте допустимый указатели параметры _lpcbEIDNewEntry_ и _lppEIDNewEntry_ . Вы несете ответственность за освобождение этот идентификатор записи после завершения с ним с помощью вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Чтобы использовать шаблон, определенного для добавления записи к контейнеру можно изменить, используйте следующую процедуру:
  
1. Вызовите метод [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия конечного контейнера и установите для параметра _lpEntryID_ значение идентификатор записи контейнера. 
    
2. Вызовите метод конечный контейнер [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и установите параметр _ulPropTag_ для **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) и параметр _lpiid_ IID_IMAPITable. Контейнер будет возвращать одноразовых таблице перечислены все шаблоны, поддерживаемые для создания новых записей. 
    
3. Получите строку, которая представляет шаблон для определенного типа записи, которую требуется создать. В столбце **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) указывается тип адреса, который поддерживается в шаблоне.
    
4. Вызовите метод **NewEntry** и установите _lpEIDNewEntryTpl_ идентификатор записи выбранного шаблона. Идентификатор записи будет столбец **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из шаблона строку в таблице одноразовых. Передайте ноль в _cbEIDContainer_ и NULL в _lpEIDContainer_. Передайте допустимый указатель в параметре _lppEIDNewEntry_ , если вы хотите сохранить идентификатор записи новую запись. 
    
## <a name="see-also"></a>См. также



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

