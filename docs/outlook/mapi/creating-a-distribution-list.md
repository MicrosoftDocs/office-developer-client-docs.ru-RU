---
title: Создание списка рассылки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f0a6b7af196073d52ce98037b443569dcd1f41e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582548"
---
# <a name="creating-a-distribution-list"></a>Создание списка рассылки

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Клиенты могут создавать список рассылки непосредственно в можно изменить контейнер, такие как личная адресная книга (адресной книги).
  
**Чтобы создать список рассылки в личной адресной книги**
  
1. Создание массива тег размера свойства с тегом одно свойство, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), следующим образом:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Вызовите [IAddrBook::GetPAB](iaddrbook-getpab.md) , чтобы получить идентификатор записи личной адресной книги. Если возникает ошибка или **GetPAB** возвращает ноль или значение NULL, не продолжайте. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) , чтобы открыть личной адресной книги. Выходной параметр _ulObjType_ должен иметь значение MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) адресной книги для получения свойства PR_DEF_CREATE_DL шаблон, который используется для создания списка рассылки. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Если не удается выполнить **GetProps** : 
    
   1. Вызов метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) адресной книги для открытия свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) с помощью интерфейса **IMAPITable** . 
      
   2. Создание ограничение свойства для поиска строк со столбцом **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)), равное «MAPIPDL». 
      
   3. Вызовите [IMAPITable::FindRow](imapitable-findrow.md) , чтобы найти этой строки. 
    
6. Сохраните идентификатор записи, возвращенный **GetProps** или **FindRow**.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Вызовите метод [IABContainer::CreateEntry](iabcontainer-createentry.md) адресной книги для создания записи с помощью шаблона, представленное идентификатор сохраненного записи. Не предполагается, что объект, возвращенный можно считать список рассылки, а не для обмена сообщениями пользователя, когда этот вызов является удаленным. Обратите внимание на то, что флаг CREATE_CHECK_DUP передается в параметре _ulFlags_ для предотвращения дважды добавления записи. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Вызовите метод **IUnknown::QueryInterface** новую запись, передав IID_IDistList идентификатор интерфейса, чтобы определить, если операция — это список рассылки и поддерживает [IDistList: IMAPIContainer](idistlistimapicontainer.md) интерфейса. Так как **CreateEntry** возвращает указатель **IMAPIProp** , а не более конкретные указатель **IMailUser** или **IDistList** , проверьте, что объект списка рассылки был создан. При успешном **QueryInterface** , можно убедиться, что вы создали в список рассылки, а не для обмена сообщениями пользователя. 
    
9. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) списка рассылки, чтобы задать его отображаемого имени и других свойств. 
    
10. Вызовите метод [IABContainer::CreateEntry](iabcontainer-createentry.md) списка рассылки, чтобы добавить одного или нескольких пользователей системы обмена сообщениями. 
    
11. Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) список рассылки, когда вы будете готовы для его сохранения. Чтобы получить идентификатор записи из списка сохраненных рассылки, установить флаг KEEP_OPEN_READWRITE, а затем вызвать [IMAPIProp::GetProps](imapiprop-getprops.md) разрешения на запрос свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
12. Освобождение список рассылки и личной адресной книги, вызвав их **функции IUnknown::Release** методы. 
    
13. Вызовите [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить память для идентификатора записи адресной книги и массива тег размера свойства. 
    

