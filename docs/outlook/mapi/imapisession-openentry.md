---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426389"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает объект и возвращает указатель интерфейса для дополнительного доступа.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи объекта, который необходимо открыть.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к открытому объекту. Передача NULL возвращает стандартный интерфейс объекта. Например, если объект, который необходимо открыть, является сообщением, стандартным интерфейсом будет [IMessage;](imessageimapiprop.md) для папок это [IMAPIFolder.](imapifolderimapicontainer.md) Стандартными интерфейсами для объектов адресной книги являются [IDistList](idistlistimapicontainer.md) для списка рассылки и [IMailUser](imailuserimapiprop.md) для пользователя обмена сообщениями. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием объекта. Можно использовать следующие флаги:
    
MAPI_BEST_ACCESS 
  
> Запрашивает открытие объекта с использованием максимального разрешения сети, разрешенного для пользователя, и максимального доступа клиентского приложения. Например, если у клиента есть разрешение на чтение и записи, объект должен быть открыт с разрешением на чтение и записи; если у клиента есть разрешение только для чтения, объект должен быть открыт с разрешением только для чтения. 
    
MAPI_CACHE_OK
  
> Используйте все средства, включая автономные адресные книги, для разрешения имен.
    
MAPI_CACHE_ONLY
  
> Используйте только автономной адресной книги для разрешения имен. Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком адресной книги Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenEntry** успешно возвращаться, возможно, до того, как объект будет полностью доступен вызываемому клиенту. Если объект не доступен, последующий вызов объекта может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию объекты открываются с разрешением только на чтение, и клиенты не должны работать при предположении, что разрешение на чтение и чтение предоставлено. 
    
MAPI_NO_CACHE
  
> Не используйте автономной адресной книги для разрешения имен. Этот флаг поддерживается только поставщиком адресной книги Exchange.
    
SHOW_SOFT_DELETES
  
> Показать элементы, которые в настоящее время помечены как "мягко удаленные" (то есть находятся на этапе хранения удаленных элементов).
    
 _lpulObjType_
  
> [out] Указатель на тип открытого объекта.
    
 _lppUnk_
  
> [out] Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект был успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка изменить объект, доступный только для чтения, или попытка доступа к объекту, у которого у пользователя недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Объект, связанный с идентификатором записи, переданным в  _параметре lpEntryID, не_ существует. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи, переданный в  _параметре lpEntryID,_ имеет неизвестный формат. Обычно это значение возвращается, если поставщик услуг, содержащий объект, не открыт. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::OpenEntry** открывает хранилище сообщений или объект адресной книги, возвращая указатель на интерфейс, который можно использовать для доступа к объекту. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

> [!IMPORTANT]
> При открытии записей в общедоступных магазинах, таких как папки и сообщения, используйте [IMsgStore::OpenEntry](imsgstore-openentry.md) вместо **IMAPISession::OpenEntry.** Это гарантирует правильную работу общедоступных папок, если в профиле определено несколько учетных записей Exchange. 
  
Вызовите **IMAPISession::OpenEntry** только в том случае, если вы не знаете, какой объект открывается. Если вы знаете, что открываете папку или сообщение, вызовите [IMsgStore::OpenEntry.](imsgstore-openentry.md) Если вы знаете, что вы открываете контейнер адресной книги, пользователя обмена сообщениями или список рассылки, вызовите [IAddrBook::OpenEntry.](iaddrbook-openentry.md) Эти более конкретные методы **быстрее, чем IMAPISession::OpenEntry.** 
  
MAPI открывает все объекты с разрешением только для чтения, если вы не MAPI_MODIFY или MAPI_BEST_ACCESS флага в параметре _ulFlags._ Установка одного из этих флагов не гарантирует определенный тип доступа; Предоставленные разрешения зависят от поставщика услуг, уровня доступа и объекта. Чтобы определить уровень доступа открытого объекта, извлекаете **его PR_ACCESS_LEVEL** ([PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)
  
Вызов **IMAPISession::OpenEntry** и настройка  _lpEntryID_ для ссылки на идентификатор записи в хранилище сообщений это то же, что вызов метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) с установленным флагом MDB_NO_DIALOG. Параметры флага также эквивалентны, за исключением того, что для запроса разрешения на чтение и записи в **OpenMsgStore** необходимо установить флаг MDB_WRITE, а не MAPI_MODIFY. 
  
Проверьте значение, возвращаемого в  _параметре lpulObjType,_ чтобы определить, является ли возвращаемого типа объекта ожидаемым. Если тип объекта не тот, который вы ожидали, приведите указатель из параметра  _lppUnk_ к указателю соответствующего типа. Например, если вы открываете папку, приведите  _lppUnk_ к указателю типа LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI использует метод **IMAPISession::OpenEntry** для открытия объекта.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

