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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиенты могут создавать список рассылки непосредственно в изменяемый контейнер, например личную адресную книгу (PAB).
  
**Создание списка рассылки в PAB**
  
1. Создайте массив тегов свойств размером с одним **тегом свойства PR_DEF_CREATE_DL** [(PidTagDefCreateDl),](pidtagdefcreatedl-canonical-property.md)следующим образом:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Вызов [IAddrBook::GetPAB](iaddrbook-getpab.md) для получения идентификатора записи PAB. Если ошибка или **GetPAB** возвращает ноль или NULL, не продолжайте. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Вызов [IAddrBook::OpenEntry,](iaddrbook-openentry.md) чтобы открыть PAB. Параметр  _вывода ulObjType_ должен быть задан для MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Чтобы получить свойство PR_DEF_CREATE_DL, шаблон, который он использует для создания списка рассылки, позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) PR_DEF_CREATE_DL PAB. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Если **сбой GetProps:** 
    
   1. Вызов  [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для открытия свойства [PR_CREATE_TEMPLATES (PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)с интерфейсом **IMAPITable.** 
      
   2. Создайте ограничение свойств для поиска строки с **помощью столбца PR_ADDRTYPE** [(PidTagAddressType),](pidtagaddresstype-canonical-property.md)равного "MAPIPDL". 
      
   3. Вызов [IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти эту строку. 
    
6. Сохраните идентификатор записи, возвращенный **getProps или** **FindRow.**
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Вызов метода [IABContainer::CreateEntry](iabcontainer-createentry.md) для создания новой записи с помощью шаблона, представленного идентификатором сохраненной записи. Не следует предполагать, что возвращаемый объект будет списком рассылки, а не пользователем обмена сообщениями при удалении этого вызова. Обратите внимание, CREATE_CHECK_DUP флаг передается в  _параметре ulFlags,_ чтобы предотвратить дваждые добавление записи. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Позвоните по методу **IUnknown::QueryInterface,** IID_IDistList в качестве идентификатора интерфейса, чтобы определить, является ли запись списком рассылки и поддерживает интерфейс [IDistList : IMAPIContainer.](idistlistimapicontainer.md) Поскольку **CreateEntry** возвращает указатель **IMAPIProp,** а не более конкретный указатель **IMailUser** или **IDistList,** проверьте, был ли создан объект списка рассылки. Если **queryInterface** успешно, вы можете быть уверены, что создали список рассылки, а не пользователя обмена сообщениями. 
    
9. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) списка рассылки, чтобы установить его имя отображения и другие свойства. 
    
10. Вызовите метод [IABContainer::CreateEntry](iabcontainer-createentry.md) в списке рассылки, чтобы добавить одного или несколько пользователей обмена сообщениями. 
    
11. Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) в списке рассылки, когда вы будете готовы его сохранить. Чтобы получить идентификатор записи сохраненного списка рассылки, установите флаг KEEP_OPEN_READWRITE, а затем позвоните [в IMAPIProp::GetProps](imapiprop-getprops.md) с запросом свойства PR_ENTRYID[(PidTagEntryId).](pidtagentryid-canonical-property.md) 
    
12. Отпустите новый список рассылки и PAB, назвав их **методы IUnknown::Release.** 
    
13. [Вызывай MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память для идентификатора записи PAB и массива тегов свойств размера. 
    

