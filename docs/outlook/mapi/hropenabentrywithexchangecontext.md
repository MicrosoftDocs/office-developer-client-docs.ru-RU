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
ms.openlocfilehash: fcedaf689db8280b4649662ba61c8468d0f98305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808683"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

  
  
**Относится к**: Outlook 
  
Открывает **entryID** , с помощью адресная книга Exchange, определяемую средством **pEmsmdbUID**. Эта функция работает так же [IAddrBook::Details](iaddrbook-details.md) за исключением того, что с помощью этой функции гарантирует, что [IAddrBook::OpenEntry](iaddrbook-openentry.md) открыто с помощью ожидаемый Exchange доступа к адресной книге. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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

## <a name="parameters"></a>Параметры

 _pmsess_
  
> [in] Система на **IMAPISession**. Он не может быть NULL.
    
 _pEmsmdbUID_
  
> [in] Указатель на **emsmdbUID** , который определяет службу Exchange, которая содержит поставщик адресной книги Exchange, который следует использовать эту функцию для отображения сведений на идентификатор записи. Если входящий идентификатор записи не идентификатор записи Exchange поставщик адресной книги, этот параметр игнорируется и вызов функции действует как [IAddrBook::Details](iaddrbook-details.md). Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция действует как [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] В адресной книге используется для открытия идентификатор записи. Он не может быть NULL.
    
 _cbEntryID_
  
> [in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ . 
    
 _lpEntryID_
  
>  [in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как открыть запись. Можно задать следующие флажки:
    
MAPI_BEST_ACCESS
  
> Запросы, что операция открываются с максимальное допустимое разрешения сети и клиента. Например если клиент чтение и запись, поставщик адресной книги пытается открыть запись с чтение и запись. Можно получить уровень доступа, который был предоставлен путем вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) open записи и извлечение свойства PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен с помощью автономной адресной книги. Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения. Этот флаг поддерживается только поставщик Exchange адресной книги.
    
MAPI_DEFERRED_ERRORS
  
> Разрешает вызов для успешного выполнения, потенциально перед словом полностью open и доступны, подразумевает, что последующие вызовы записи могут завершиться ошибкой.
    
MAPI_GAL_ONLY
  
> Для выполнения разрешения имен используется только глобальный список адресов. Этот флаг поддерживается только поставщик Exchange адресной книги.
    
MAPI_MODIFY
  
> Запросы, которые словом открывать с чтение и запись. Поскольку записи открываются с доступом только для чтения по умолчанию, клиенты не следует предполагать, чтение и запись, независимо от того, является ли задать MAPI_MODIFY были предоставлены разрешения.
    
MAPI_NO_CACHE
  
> Не используйте автономной адресной книги для разрешения имен. Этот флаг поддерживается только поставщик Exchange адресной книги.
    

