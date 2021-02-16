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
ms.openlocfilehash: 7108ae215562169244100a56cc9b9208d78b1893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424177"
---
# <a name="creating-a-distribution-list"></a>Создание списка рассылки

**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты могут создать список рассылки непосредственно в изменяемом контейнере, например в личной адресной книге.
  
**Создание списка рассылки в PAB**
  
1. Создайте массив тегов свойств размера с одним тегом свойства **PR_DEF_CREATE_DL** ([PidTagDefCreateDl),](pidtagdefcreatedl-canonical-property.md)следующим образом:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Вызовите [IAddrBook::GetPAB,](iaddrbook-getpab.md) чтобы получить идентификатор записи для PAB. Если произошла ошибка или **GetPAB** возвращает ноль или значение NULL, не продолжайте. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Вызовите [IAddrBook::OpenEntry,](iaddrbook-openentry.md) чтобы открыть PAB. Выходной  _параметр ulObjType_ должен иметь MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) для получения свойства PR_DEF_CREATE_DL, шаблона, который используется для создания списка рассылки. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Если **сбой GetProps:** 
    
   1. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для PAB, чтобы открыть **свойство PR_CREATE_TEMPLATES** ([PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)с интерфейсом **IMAPITable.** 
      
   2. Создайте ограничение свойств для поиска строки со **столбцом PR_ADDRTYPE** ([PidTagAddressType),](pidtagaddresstype-canonical-property.md)равным "MAPIPDL". 
      
   3. Вызовите [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти эту строку. 
    
6. Сохраните идентификатор записи, возвращенный **getProps** или **FindRow.**
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Вызовите метод [IABContainer::CreateEntry для PAB,](iabcontainer-createentry.md) чтобы создать новую запись с помощью шаблона, представленного сохраненным идентификатором записи. При удалении этого вызова не следует предполагать, что возвращенный объект будет списком рассылки, а не пользователем системы обмена сообщениями. Обратите внимание, CREATE_CHECK_DUP флаг передается в  _параметре ulFlags,_ чтобы запись не добавлялась дважды. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Вызовите метод **IUnknown::QueryInterface** новой записи, передав IID_IDistList в качестве идентификатора интерфейса, чтобы определить, является ли запись списком рассылки и поддерживает интерфейс [IDistList : IMAPIContainer.](idistlistimapicontainer.md) Поскольку **CreateEntry** возвращает указатель **IMAPIProp,** а не более конкретный указатель **IMailUser** или **IDistList,** убедитесь, что объект списка рассылки создан. Если **queryInterface** успешно, вы можете быть уверены, что вы создали список рассылки, а не пользователя обмена сообщениями. 
    
9. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) списка рассылки, чтобы установить его отображаемую и другие свойства. 
    
10. Вызовите метод [IABContainer::CreateEntry](iabcontainer-createentry.md) списка рассылки, чтобы добавить одного или несколько пользователей обмена сообщениями. 
    
11. Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) списка рассылки, когда будете готовы сохранить его. Чтобы получить идентификатор записи сохраненного списка рассылки, установите флаг KEEP_OPEN_READWRITE и вызовите [IMAPIProp::GetProps,](imapiprop-getprops.md) **запрашивающий** свойство PR_ENTRYID ([PidTagEntryId).](pidtagentryid-canonical-property.md)
    
12. Освободите новый список рассылки и PAB, вызывая их методы **IUnknown::Release.** 
    
13. Вызовите [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память для идентификатора записи PAB и массива тегов свойств размера. 
    

