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
ms.openlocfilehash: 6234fc737857a7e35f562703802f81ff154b3ee6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591018"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Открывает объект и возвращает указатель интерфейса для дополнительные права доступа.
  
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
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на запись идентификатор объекта для открытия.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту открыт. Передача NULL Возвращает стандартный интерфейс объекта. Например если к объекту, чтобы открыть сообщение, стандартный интерфейс будет [IMessage](imessageimapiprop.md); для папок это [IMAPIFolder](imapifolderimapicontainer.md). Стандартные интерфейсы для объектов адресной книги — [IDistList](idistlistimapicontainer.md) для списка рассылки, а также [IMailUser](imailuserimapiprop.md) для обмена сообщениями пользователя. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет способ открытия объекта. Можно использовать следующие флажки:
    
MAPI_BEST_ACCESS 
  
> Запрашивает открыть объект с помощью максимальное сетевое разрешения для пользователя и приложения максимальное клиентского доступа. Например если клиент имеет разрешение на чтение и запись, объект должен быть открыт получившие разрешение на чтение и запись; Если клиент имеет разрешение на чтение, объект должен быть открыт с разрешением только для чтения. 
    
MAPI_CACHE_OK
  
> Для выполнения разрешения имен используйте все это значит, включая автономные адресные книги.
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен используйте автономной адресной книги. Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения. Этот флаг поддерживается только поставщик Exchange адресной книги.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenEntry** для возврата успешно, возможно перед объект полностью доступен для клиента. Если объект недоступен, вызов последующих объектов может вызвать ошибку. 
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию объекты открываются с разрешением только для чтения, и клиенты не должны работать предполагается, что что разрешение чтения и записи. 
    
MAPI_NO_CACHE
  
> Не используйте автономной адресной книги для разрешения имен. Этот флаг поддерживается только поставщик Exchange адресной книги.
    
SHOW_SOFT_DELETES
  
> Отображение удаленных элементов, которые в настоящее время помечены как программных (то есть, они находятся в хранения удаленных элементов этап времени).
    
 _lpulObjType_
  
> [out] Указатель на тип объекта открыт.
    
 _lppUnk_
  
> [out] Указатель на указатель на объект открыт.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Объект был успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Попытка изменить объект только для чтения или предпринята попытка получить доступ к объекту, для которого пользователь имеет недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Объект, связанный с идентификатором записи, переданной в параметре _lpEntryID_ не существует. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи, переданной в параметре _lpEntryID_ имеет неопознанный формат. Это значение возвращается как правило, если поставщик услуг, содержащее объект не открыт. 
    
## <a name="remarks"></a>Замечания

Открывает метод **IMAPISession::OpenEntry** сообщение хранения или адрес объекта книги, указатель возвращается интерфейс, который можно использовать для доступа к объекту. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

> [!IMPORTANT]
> При открытии записи папки для общего хранилища, например, папок и сообщений, используйте [IMsgStore::OpenEntry](imsgstore-openentry.md) вместо **IMAPISession::OpenEntry**. Это обеспечить общедоступные папки правильное функционирование при определении нескольких учетных записей Exchange в профиле. 
  
Вызов **IMAPISession::OpenEntry** только в том случае, если вы не знаете, какой тип объекта, который открывается. Если вы знаете, что открывают папки или сообщения, вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md). Если вы знаете, что открываемый контейнер адресной книги, обмена мгновенными сообщениями пользователя или список рассылки, вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md). Эти дополнительные методы выполняются быстрее, чем **IMAPISession::OpenEntry**. 
  
MAPI открывает все объекты с разрешением только для чтения, если не задан флаг MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags_ . Настройка одного из этих флагов не гарантирует определенным типом доступа; разрешения, предоставленные зависят от поставщика услуг, уровень доступа и объект. Чтобы определить уровень доступа для открытого объекта, получения его свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Вызов **IMAPISession::OpenEntry** и параметр _lpEntryID_ для указания на идентификатор записи хранилища сообщений имеет то же, что вызов метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) с флагом MDB_NO_DIALOG значение. Параметры флаг эквивалентны также, за исключением, для получения разрешения чтения и записи с **OpenMsgStore**, необходимо установить флаг MDB_WRITE вместо MAPI_MODIFY. 
  
Проверьте значение, возвращенное в параметре _lpulObjType_ , чтобы определить, является ли тип объекта, возвращенного ожидаемого. Если тип объекта не тип, который вы неправильно, приведение указателя с помощью параметра _lppUnk_ указатель соответствующего типа. Например при открытии папки привести _lppUnk_ для указателя типа LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |Mfcmapi (en) использует метод **IMAPISession::OpenEntry** для открытия объекта.  <br/> |
   
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

