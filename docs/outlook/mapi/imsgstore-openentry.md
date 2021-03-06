---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409337"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает папку или сообщение и возвращает указатель интерфейса для дальнейшего доступа. 
  
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
  
> [in] Количество byte в идентификаторе входа, на который указывает  параметр _lpEntryID._
    
 _lpEntryID_
  
> [in] Указатель на идентификатор входа открываемого объекта или NULL. Если  _lpEntryID_ задан nULL, **OpenEntry** открывает корневую папку для магазина сообщений. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к открытому объекту. Передача NULL приводит к возвращению стандартного интерфейса объекта[(IMAPIFolder](imapifolderimapicontainer.md) для папок и [IMessage](imessageimapiprop.md) для сообщений). 
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается объект. Можно использовать следующие флаги:
    
MAPI_BEST_ACCESS 
  
> Запрашивает, чтобы объект был открыт с помощью максимально допустимых разрешений сети для пользователя и максимального доступа к приложениям клиента. Например, если у клиента есть разрешение на чтение и записи, объект должен быть открыт с помощью разрешения на чтение и записи; если у клиента есть разрешение только для чтения, объект должен быть открыт с помощью разрешения только для чтения. 
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenEntry** успешно возвращаться, возможно, до того, как объект будет полностью доступен вызываемому клиенту. Если объект не доступен, при последующем вызове объекта может быть допущена ошибка. 
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию объекты открываются только для чтения, и клиенты не должны работать с предположением о том, что разрешение на чтение и записи предоставляется. 
    
 _lpulObjType_
  
> [вышел] Указатель на тип открываемого объекта.
    
 _lppUnk_
  
> [вышел] Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка изменить объект только для чтения или получить доступ к объекту, для которого у пользователя недостаточно разрешений.
    
MAPI_NO_CACHE
  
> Когда магазин открыт в кэшном режиме, клиент или поставщик услуг может вызвать **IMsgStore::OpenEntry,** установив флаг MAPI_NO_CACHE, чтобы открыть элемент или папку в удаленном магазине. Если вы откроете хранилище сообщений с флагом MDB_ONLINE на удаленном сервере, вам не нужно использовать MAPI_NO_CACHE флаг.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::OpenEntry** открывает папку или сообщение и возвращает указатель в интерфейс, который можно использовать для дальнейшего доступа. 
  
> [!IMPORTANT]
> При открытии записей папок в общедоступных магазинах, таких как папки и сообщения, используйте **IMsgStore::OpenEntry** вместо [IMAPISession::OpenEntry.](imapisession-openentry.md) Это обеспечивает правильную работу общедоступных папок при Exchange нескольких учетных записей в профиле. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Папки и сообщения автоматически открываются с разрешения только для чтения, если в параметре  _ulFlags_ MAPI_MODIFY или MAPI_BEST_ACCESS флаг. Установка одного из этих флагов не гарантирует определенный тип разрешения; разрешения, которые вы получили, зависят от поставщика магазина сообщений, уровня доступа и объекта. Чтобы определить уровень доступа открываемого  объекта, PR_ACCESS_LEVEL[(PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)
  
Хотя **IMsgStore::OpenEntry** можно использовать для открытия любой папки или сообщения, обычно быстрее использовать метод [IMAPIContainer::OpenEntry,](imapicontainer-openentry.md) если у вас есть доступ к родительской папке папки или сообщению, которые необходимо открыть. 
  
Проверьте значение, возвращаемого в  _параметре lpulObjType,_ чтобы определить, является ли тип возвращаемого объекта ожидаемым. Если тип объекта не является ожидаемым, отведите указатель из параметра  _lppUnk_ в указатель соответствующего типа. Например, если вы открываете папку, отведите  _lppUnk_ в указатель типа **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI использует **метод IMsgStore::OpenEntry** для открытия объекта, связанного с ИД входа.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

