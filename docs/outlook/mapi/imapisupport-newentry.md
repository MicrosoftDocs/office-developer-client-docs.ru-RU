---
title: IMAPISupportNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d978b7a6bd8af9a505fa025aef2e5da68308468f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588596"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет нового получателя непосредственно к контейнеру адресной книги или списка получателей исходящих сообщений.
  
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
  
> [in] Дескриптор родительского окна диалогового окна.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _cbEIDContainer_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [in] Указатель на идентификатор записи контейнера для получения новая запись. Если _cbEIDContainer_ равно 0 и _lpEIDContainer_ имеет значение NULL, **NewEntry** создает идентификатор единичных записей, который имеет тот же тип, как создается путем вызова метода [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [in] Указатель на идентификатор записи шаблона, который используется для создания новой записи. Если _cbEIDNewEntryTpl_ равно 0 и _lpEIDNewEntryTpl_ имеет значение NULL, **NewEntry** отображает диалоговое окно, которое позволяет пользователям выбирать из списка шаблонов для добавления новых записей. 
    
 _lpcbEIDNewEntry_
  
> [out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Указатель на указатель на идентификатор операции записи в только что созданный.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новая запись успешно создан.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::NewEntry** реализуется для объектов поддержки поставщик адресной книги. Поставщиками адресной книги вызовите **NewEntry** , чтобы создать новую запись книги адрес добавляемого непосредственно в контейнер или для использования с учетом исходящих сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Новая запись будет добавлена к конкретному контейнеру, установите _lpEIDContainer_ идентификатор записи и _cbEIDContainer_ на число байтов в идентификатор записи контейнера. 
  
Новая запись будет добавлена в список получателей исходящих сообщений, установите _lpEIDContainer_ NULL и _cbEIDContainer_ значение 0. 
  
Если вы хотите разрешить пользователю создавать клиентского приложения, чтобы выбрать тип записи, передайте 0 в _cbEIDNewEntryTpl_ и NULL в _lpEIDNewEntryTpl_. **NewEntry** отображаются в таблице одноразовых MAPI, список шаблонов, которые поддерживают MAPI и каждый из поставщиками адресной книги в сеансе. В каждый шаблон можно создать запись получателей для одного или нескольких типов адресов. 
  
Если вы хотите сохранить идентификатор записи новой записи, передайте допустимый указатели параметры _lpcbEIDNewEntry_ и _lppEIDNewEntry_ . Вы несете ответственность за освобождение этот идентификатор записи после завершения с ним с помощью вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Чтобы использовать шаблон, определенного для добавления записи к контейнеру можно изменить, используйте следующую процедуру:
  
1. Вызовите метод [IMAPISupport::OpenEntry](imapisupport-openentry.md) для открытия конечного контейнера и установите для параметра _lpEntryID_ значение идентификатор записи контейнера. 
    
2. Вызовите метод конечный контейнер [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и установите параметр _ulPropTag_ для **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) и параметр _lpiid_ IID_IMAPITable. Контейнер будет возвращать одноразовых таблице перечислены все шаблоны, поддерживаемые для создания новых записей. 
    
3. Получите строку, которая представляет шаблон для определенного типа записи, которую требуется создать. В столбце **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) указывается тип адреса, который поддерживается в шаблоне. 
    
4. Вызовите **IMAPISupport::NewEntry** и установите для параметра _lpEIDNewEntryTpl_ значение идентификатор записи выбранного шаблона. Идентификатор записи — это столбец **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из шаблона строку в таблице одноразовых. Передайте 0 в _cbEIDContainer_ и NULL в _lpEIDContainer_. Передайте допустимый указатель в параметре _lppEIDNewEntry_ , если вы хотите сохранить идентификатор записи новую запись. 
    
## <a name="see-also"></a>См. также



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

