---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429910"
---
# <a name="hropenabentrywithresolvedrow"></a>HrOpenABEntryWithResolvedRow

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполняет ту же функцию, что [и HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) за исключением того, что он автоматически получает **emsabpUID** из разрешенной строки и открывает **entryID**.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _prwResolved_
  
> [in] Указатель на разрешенную строку, которая используется для получения **emsabpUID** и открытия **entryID**.
    
 _pAddrBook_
  
> [in] Адресная книга, используемая для открытия идентификатора записи. Это не может быть NULL.
    
 _cbEntryID_
  
> [in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter. 
    
 _lpEntryID_
  
>  [in] Указатель на идентификатор записи, который представляет открытую запись адресной книги. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) интерфейса, который используется для доступа к открытой записи. Передача NULL возвращает стандартный интерфейс объекта. Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md). Для списков рассылки это [IDistList: IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Звонители могут настроить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования. 
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается запись. Можно установить следующие флаги:
    
MAPI_BEST_ACCESS
  
> Запросы на открытие записи с максимально разрешенными сетевыми и клиентными разрешениями. Например, если клиент имеет разрешение на чтение и запись, поставщик адресной книги пытается открыть запись с разрешения на чтение и запись. Клиент может получить уровень доступа, который был предоставлен, позвонив [методу IMAPIProp::GetProps](imapiprop-getprops.md) открытой записи и извлекая свойство PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен используется только офлайн-адресная книга. Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в кэшном режиме обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком Exchange адресной книги.
    
MAPI_DEFERRED_ERRORS
  
> Позволяет добиться успеха вызова, потенциально до того, как запись будет полностью открыта и доступна, что означает, что последующие вызовы в запись могут привести к ошибке.
    
MAPI_GAL_ONLY
  
> Для выполнения разрешения имен используется только GAL. Этот флаг поддерживается только поставщиком Exchange адресной книги.
    
MAPI_MODIFY
  
> Запросы на открытие записи с разрешения на чтение и запись. Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не должны предполагать, что разрешение на чтение и запись было предоставлено независимо от того, MAPI_MODIFY установлено.
    
MAPI_NO_CACHE
  
> Не использует автономной адресной книги для выполнения разрешения имен. Этот флаг поддерживается только поставщиком Exchange адресной книги.
    
 _lpulObjType_
  
> [вышел] Указатель на тип открываемой записи.
    
 _lppUnk_
  
> [вышел] Указатель на указатель открываемой записи.
    

