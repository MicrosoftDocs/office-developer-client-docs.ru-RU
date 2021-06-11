---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409232"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель в реализацию интерфейса, чтобы обеспечить дополнительный доступ.
  
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
  
> [in] Указатель на идентификатор входа для открываемого контейнера, пользователя обмена сообщениями или списка рассылки.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к открытому объекту. Передача NULL возвращает идентификатор для стандартного интерфейса объекта. Для контейнеров стандартным интерфейсом [является IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Стандартными интерфейсами для объектов адресной книги являются [IDistList: IMAPIContainer](idistlistimapicontainer.md) для списка рассылки и [IMailUser: IMAPIProp](imailuserimapiprop.md) для пользователя обмена сообщениями. 
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается объект. Можно установить следующие флаги:
    
MAPI_BEST_ACCESS 
  
> Запрашивает, чтобы объект был открыт с максимальным разрешением сети, разрешенным для пользователя, и максимальным доступом к приложению клиента. Например, если у клиента есть разрешение на чтение и записи, объект должен быть открыт с разрешения на чтение и записи; если у клиента есть разрешение только для чтения, объект должен быть открыт только для чтения.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **методу OpenEntry** успешно возвращаться, возможно, до полного доступа к объекту клиент-вызов. Если объект не имеет доступа, при последующем вызове объекта может быть допущена ошибка. 
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию объекты открываются с доступом только для чтения, и клиенты не должны предполагать, что разрешение на чтение и записи было предоставлено.
    
 _lpulObjType_
  
> [вышел] Указатель на тип открываемого объекта.
    
 _lppUnk_
  
> [вышел] Указатель на указатель на открытый объект.
    
## <a name="remarks"></a>Примечания

S_OK 
  
> Объект был успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Либо у пользователя недостаточно разрешений на открытие объекта, либо была предпринята попытка открыть объект только для чтения с разрешения на чтение и написание.
    
MAPI_E_NOT_FOUND 
  
> Идентификатор записи, указанный  _lpEntryID,_ не представляет объекта. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи в параметре  _lpEntryID_ не имеет формата, распознаемого поставщиком адресной книги. 
    
## <a name="remarks"></a>Примечания

MAPI вызывает метод **OpenEntry** для открытия контейнера, пользователя обмена сообщениями или списка рассылки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Прежде чем MAPI вызывает метод **OpenEntry,** он определяет, что идентификатор входа в  _параметре lpEntryID_ принадлежит вам, а не другому поставщику. MAPI делает это путем совпадения структуры [MAPIUID](mapiuid.md) в идентификаторе входа с **MAPIUID,** который вы зарегистрировали, позвонив [методу IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) при запуске. 
  
Откройте объект только для чтения, если MAPI_MODIFY или MAPI_BEST_ACCESS в параметре _ulFlags._ Если вы не разрешаете изменение запрашиваемой цели, не открывайте объект вообще и возвращайте MAPI_E_NO_ACCESS. 
  
Если MAPI передает NULL для  _lpEntryID,_ откройте корневой контейнер в иерархии контейнеров.
  
Объект, который требуется открыть, может быть объектом, скопированным у другого поставщика. В этом случае он будет поддерживать свойство **PR_TEMPLATEID** [(PidTagTemplateid).](pidtagtemplateid-canonical-property.md) Если объект поддерживает это свойство, позвоните по методу [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) для привязки  к коду для этой записи в иностранном поставщике, PR_TEMPLATEID в _параметре lpTemplateID_ и 0 в _параметре ulTemplateFlags._ **IMAPISupport::OpenTemplateID** передает эти сведения иностранному поставщику по вызову метода [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) иностранного поставщика. Если **IMAPISupport::OpenTemplateID** вызывает ошибку, как правило, потому, что иностранный поставщик недоступен или не включен в профиль, попробуйте продолжить, обрабатывая неограниченную запись только для чтения. Дополнительные сведения об открытии записей иностранных адресных книг см. в [статьях Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>См. также



[IABLogon : IUnknown](iablogoniunknown.md)

