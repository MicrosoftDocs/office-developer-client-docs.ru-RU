---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eb91f4998f94ffafbc33b6024228945f7c91cf43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564992"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает книги два адреса **entryIDs** безопасно в профиле нескольких Exchange. Эта функция — это функция замены для [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a>Параметры

 _pmsess_
  
> [in] Система на **IMAPISession**. Он не может быть NULL.
    
 _pEmsmdbUID_
  
> [in] Указатель на **emsmdbUID** , который определяет службу Exchange, которая содержит поставщик адресной книги Exchange, который следует использовать эту функцию для отображения сведений на идентификатор записи. Если входящий идентификатор записи не идентификатор записи Exchange поставщик адресной книги, этот параметр игнорируется и вызов функции действует как [IAddrBook::Details](iaddrbook-details.md). Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция действует как [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] В адресной книге используется для открытия идентификатор записи. Он не может быть NULL.
    
 _cbEntryID1_
  
> [in] Количество байтов первой записи идентификатор, указанный в параметре _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи, который представляет записи адресной книги для сравнения.
    
 _cbEntryID2_
  
> [in] Количество байтов второй идентификатор записи, указанные с помощью параметра _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Указатель на втором запись идентификатор, который используется для сравнения, представляющий запись адресной книги для сравнения.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на папку, где содержатся результаты сравнения. 
    

