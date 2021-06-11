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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор входа объекта для открытия.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к открытому объекту. Передача NULL возвращает стандартный интерфейс объекта. Например, если объект, который будет открыт, является сообщением, стандартным интерфейсом [является IMessage;](imessageimapiprop.md) для папок это [IMAPIFolder](imapifolderimapicontainer.md). Стандартными интерфейсами для объектов адресной книги являются [IDistList](idistlistimapicontainer.md) для списка рассылки и [IMailUser](imailuserimapiprop.md) для пользователя обмена сообщениями. 
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается объект. Можно использовать следующие флаги:
    
MAPI_BEST_ACCESS 
  
> Запрашивает, чтобы объект был открыт с помощью максимально допустимых разрешений сети для пользователя и максимального доступа к приложениям клиента. Например, если у клиента есть разрешение на чтение и записи, объект должен быть открыт с разрешения на чтение и записи; если у клиента есть разрешение только для чтения, объект должен быть открыт только для чтения. 
    
MAPI_CACHE_OK
  
> Используйте все средства, включая автономные адресные книги, для выполнения разрешения имен.
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен используйте только офлайн-адресную книгу. Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в кэшном режиме обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком Exchange адресной книги.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenEntry** успешно возвращаться, возможно, до того, как объект будет полностью доступен вызываемому клиенту. Если объект не доступен, последующий вызов объекта может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию объекты открываются только для чтения, и клиенты не должны работать с предположением о том, что разрешение на чтение и записи предоставляется. 
    
MAPI_NO_CACHE
  
> Не используйте офлайн-адресную книгу для выполнения разрешения имен. Этот флаг поддерживается только поставщиком Exchange адресной книги.
    
SHOW_SOFT_DELETES
  
> Показать элементы, которые в настоящее время помечены как мягкие удаленные (то есть они находятся на этапе хранения удаленных элементов).
    
 _lpulObjType_
  
> [вышел] Указатель на тип открываемого объекта.
    
 _lppUnk_
  
> [вышел] Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект был открыт успешно.
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка изменить объект только для чтения, или была предпринята попытка доступа к объекту, для которого у пользователя недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> В параметре  _lpEntryID_ не существует объекта, связанного с идентификатором записи. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи, переданный в  _параметре lpEntryID,_ находится в неузнаваемом формате. Обычно это значение возвращается, если поставщик услуг, содержащий объект, не открыт. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::OpenEntry** открывает хранилище сообщений или объект адресной книги, возвращая указатель интерфейсу, который можно использовать для доступа к объекту. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

> [!IMPORTANT]
> При открытии записей папок в общедоступных магазинах, таких как папки и сообщения, используйте [IMsgStore::OpenEntry](imsgstore-openentry.md) вместо **IMAPISession::OpenEntry.** Это обеспечивает правильную работу общедоступных папок при Exchange нескольких учетных записей в профиле. 
  
Вызов **IMAPISession::OpenEntry** только в том случае, если вы не знаете, какой объект вы открываете. Если вы знаете, что открываете папку или сообщение, позвоните [в IMsgStore::OpenEntry](imsgstore-openentry.md). Если вы знаете, что вы открываете контейнер адресной книги, пользователя обмена сообщениями или список рассылки, позвоните [в IAddrBook::OpenEntry](iaddrbook-openentry.md). Эти более конкретные методы быстрее, чем **IMAPISession::OpenEntry**. 
  
MAPI открывает все объекты только для чтения, если в параметре  _ulFlags_ MAPI_MODIFY или MAPI_BEST_ACCESS флаг. Установка одного из этих флагов не гарантирует определенный тип доступа; выданные разрешения зависят от поставщика услуг, уровня доступа и объекта. Чтобы определить уровень доступа открываемого  объекта, PR_ACCESS_LEVEL[(PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)
  
Вызов **IMAPISession::OpenEntry** и установка  _lpEntryID_ для указать на идентификатор входа в хранилище сообщений то же самое, что вызывать метод [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) с набором флагов MDB_NO_DIALOG. Параметры флага также эквивалентны, за исключением того, что для запроса разрешения на чтение и записи в **OpenMsgStore** необходимо установить флаг MDB_WRITE вместо MAPI_MODIFY. 
  
Проверьте значение, возвращаемого в  _параметре lpulObjType,_ чтобы определить, является ли возвращенный тип объекта ожидаемым. Если тип объекта не является ожидаемым типом, отведите указатель из параметра  _lppUnk_ в указатель соответствующего типа. Например, если вы открываете папку, введите  _lppUnk_ в указатель типа LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI использует **метод IMAPISession::OpenEntry** для открытия объекта.  <br/> |
   
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

