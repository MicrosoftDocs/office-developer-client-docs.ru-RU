---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434342"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет ту же функцию, что и [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) за исключением того, что в качестве параметра _pEmsmdbUID_ используется устаревшая версия **emsmdbUID.** Не используйте эту функцию, если не удается получить правильный **emsmdbUID** для вызова [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Параметры

 _pmsess_
  
> [in] Во время входа в **систему IMAPISession.** Это не может быть NULL.
    
 _pAddrBook_
  
> [in] Адресная книга, используемая для открытия идентификатора записи. Это не может быть NULL.
    
 _cbEntryID_
  
> [in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._ 
    
 _lpEntryID_
  
>  [in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса, используемый для доступа к открытой записи. Передача NULL возвращает стандартный интерфейс объекта. Для пользователей обмена сообщениями стандартным интерфейсом [является IMailUser : IMAPIProp](imailuserimapiprop.md). Для списков рассылки это [IDistList : IMAPIContainer,](idistlistimapicontainer.md)а для контейнеров — [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Вызывающие могут установить  _lpInterface_ для соответствующего стандартного интерфейса или интерфейса в иерархии наследования. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием записи. Можно установить следующие флаги:
    
MAPI_BEST_ACCESS
  
> Запрашивает открытие записи с максимальным разрешенным доступом к сети и разрешениям клиента. Например, если у клиента есть разрешение на чтение и запись, поставщик адресной книги пытается открыть запись с разрешением на чтение и запись. Клиент может получить уровень доступа, предоставленный путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) открытой записи и получения свойства PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Для разрешения имен используется только автономной адресной книги. Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком адресной книги Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Позволяет добиться успешного вызова, возможно, до того, как запись будет полностью открытой и доступной, что означает, что последующие вызовы записи могут возвращать ошибку.
    
MAPI_GAL_ONLY
  
> Для разрешения имен используется только gal. Этот флаг поддерживается только поставщиком адресной книги Exchange.
    
MAPI_MODIFY
  
> Запрашивает открытие записи с разрешением на чтение и запись. Так как по умолчанию записи открываются с доступом только для чтения, клиенты не должны предполагать, что разрешение на чтение и запись было предоставлено независимо от того, MAPI_MODIFY настроены.
    
MAPI_NO_CACHE
  
> Не использует автономной адресной книги для разрешения имен. Этот флаг поддерживается только поставщиком адресной книги Exchange.
    
 _lpulObjType_
  
> [out] Указатель на тип открытой записи.
    
 _lppUnk_
  
> [out] Указатель на указатель открытой записи.
    

