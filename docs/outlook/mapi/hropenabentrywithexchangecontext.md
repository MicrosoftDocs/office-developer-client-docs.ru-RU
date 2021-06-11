---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434055"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает **entryID** с помощью Exchange адресной книги, идентифицированной **pEmsmdbUID.** Эта функция работает аналогично [IAddrBook::D etails,](iaddrbook-details.md) за исключением того, что использование этой функции обеспечивает открытие [IAddrBook::OpenEntry](iaddrbook-openentry.md) с помощью ожидаемого поставщика адресных книг Exchange. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _pmsess_
  
> [in] Журнал на **IMAPISession**. Это не может быть NULL.
    
 _pEmsmdbUID_
  
> [in] Указатель на **emsmdbUID,** который идентифицирует службу Exchange, которая содержит поставщик адресных книг Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи. Если идентификатор входной записи не является идентификатором Exchange поставщика адресных книг, этот параметр игнорируется, и вызов функции ведет себя так же, как [iAddrBook::D etails](iaddrbook-details.md). Если этот параметр является NULL или нулевой MAPIUID, эта функция ведет себя как [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Адресная книга, используемая для открытия идентификатора записи. Это не может быть NULL.
    
 _cbEntryID_
  
> [in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter. 
    
 _lpEntryID_
  
>  [in] Указатель на идентификатор записи, который представляет открытую запись адресной книги. 
    
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
    

