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
ms.openlocfilehash: 9572f44f1f4865fcce5d7aa8bd8478340b0de968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594721"
---
# <a name="hropenabentrywithresolvedrow"></a>HrOpenABEntryWithResolvedRow

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет те же функции, что [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , за исключением того, автоматически получает **emsabpUID** из строки возможности разрешения и открывает **entryID**.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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

## <a name="parameters"></a>Параметры

 _prwResolved_
  
> [in] Указатель на разрешить строку, в которой используется для получения **emsabpUID** и откройте **entryID**.
    
 _pAddrBook_
  
> [in] В адресной книге используется для открытия идентификатор записи. Он не может быть NULL.
    
 _cbEntryID_
  
> [in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ . 
    
 _lpEntryID_
  
>  [in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть. 
    
 _lpInterface_
  
> [in] Указатель на интерфейс идентификатор (ИД интерфейса) интерфейс, который используется для доступа к открытой операцией. Передача NULL Возвращает стандартный интерфейс объекта. Для пользователей, обмена мгновенными сообщениями, — это стандартный интерфейс [IMailUser: IMAPIProp](imailuserimapiprop.md). Для списков рассылки — это [IDistList: IMAPIContainer](idistlistimapicontainer.md)и для контейнеров, это [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Вызывающие объекты можно задать _lpInterface_ соответствующий стандартный интерфейс или интерфейс в иерархии наследования. 
    
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
    
 _lpulObjType_
  
> [out] Указатель на тип открыт записи.
    
 _lppUnk_
  
> [out] Указатель на указатель открыт записи.
    

