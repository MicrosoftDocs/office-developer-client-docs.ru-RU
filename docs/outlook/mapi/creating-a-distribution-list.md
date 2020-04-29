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
  
Клиенты могут создавать списки рассылки непосредственно в изменяемом контейнере, например в личной адресной книге (PAB).
  
**Создание списка рассылки в личной адресной книге**
  
1. Создайте массив тегов свойств с одним тегом свойства, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), как показано ниже:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Call [IAddrBook:: жетпаб](iaddrbook-getpab.md) для получения идентификатора записи личной адресной книги. Если возникает ошибка или **жетпаб** возвращает ноль или null, не продолжайте. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Call [IAddrBook:: OpenEntry](iaddrbook-openentry.md) для открытия личной адресной книги. Параметру OUTPUT _улобжтипе_ должно быть присвоено значение MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Вызовите метод [IMAPIProp::/PROPS](imapiprop-getprops.md) PAB PAB, чтобы получить свойство PR_DEF_CREATE_DL, шаблон, который он использует для создания списка рассылки. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Если не удается выполнить команду **PROPS** : 
    
   1. Вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) личной адресной книги, чтобы открыть свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) с помощью интерфейса **IMAPITable** . 
      
   2. Создайте ограничение свойства для поиска строки со столбцом **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)), равным "мапипдл". 
      
   3. Call [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения этой строки. 
    
6. Сохраните идентификатор записи, возвращенный с помощью метода/ **PROPS** , или метода **FindRow**.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Вызовите метод [иабконтаинер:: КРЕАТИНТРИ](iabcontainer-createentry.md) PAB, чтобы создать новую запись, используя шаблон, представленный сохраненным идентификатором записи. Не следует предполагать, что возвращаемый объект будет списком рассылки, а не пользователем обмена сообщениями при удаленном вызове. Обратите внимание, что флаг CREATE_CHECK_DUP передается в параметре _ulFlags_ , чтобы не допустить Добавление записи дважды. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Вызовите метод **IUnknown:: QueryInterface** новой записи, передав IID_IDistList в качестве идентификатора интерфейса, чтобы определить, является ли запись списком рассылки, и поддерживает интерфейс [идистлист: IMAPIContainer](idistlistimapicontainer.md) . Так как **креатинтри** возвращает указатель **IMAPIProp** , а не более конкретный указатель **имаилусер** или **идистлист** , убедитесь, что был создан объект списка рассылки. Если **QueryInterface** завершается успешно, вы можете убедиться, что вы создали список рассылки, а не пользователя обмена сообщениями. 
    
9. Вызовите метод [IMAPIProp:: SetProps](imapiprop-setprops.md) списка рассылки, чтобы задать отображаемое имя и другие свойства. 
    
10. Вызовите метод [иабконтаинер:: креатинтри](iabcontainer-createentry.md) списка рассылки, чтобы добавить одного или нескольких пользователей системы обмена сообщениями. 
    
11. Вызовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) списка рассылки, когда будете готовы сохранить его. Чтобы получить идентификатор записи сохраненного списка рассылки, установите флаг KEEP_OPEN_READWRITE и затем Call [IMAPIProp::-PROPS](imapiprop-getprops.md) , запрашивающие свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
12. Освободите новый список рассылки и личную личную книгу, вызвав их методы **выпусков:: Release** . 
    
13. Вызовите [мапифрибуффер](mapifreebuffer.md) , чтобы освободить память для идентификатора записи для массива тегов свойств PAB и Letter. 
    

