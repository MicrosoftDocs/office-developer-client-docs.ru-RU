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
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436435"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Безопасно сравнивает два **адресатов** в профиле Exchange с несколькими адресными книгами. Эта функция заменяет функцию [IAddrBook::CompareEntryIDs.](iaddrbook-compareentryids.md)
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |abhelp.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
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
  
> [in] Во время входа в **систему IMAPISession.** Это не может быть NULL.
    
 _pEmsmdbUID_
  
> [in] Указатель на **emsmdbUID,** который определяет службу Exchange, которая содержит поставщика адресной книги Exchange, которую эта функция должна использовать для отображения сведений об идентификаторе записи. Если идентификатор входной записи не является идентификатором записи поставщика адресной книги Exchange, этот параметр игнорируется, и вызов функции ведет себя так же, как [iAddrBook::D etails](iaddrbook-details.md). Если этот параметр имеет значение NULL или mapIUID нулевого уровня, эта функция ведет себя как [IAddrBook::D etails.](iaddrbook-details.md)
    
 _pAddrBook_
  
> [in] Адресная книга, используемая для открытия идентификатора записи. Это не может быть NULL.
    
 _cbEntryID1_
  
> [in] Количество вахтов первого идентификатора записи, указанного параметром _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Указатель на идентификатор первой записи, который представляет запись адресной книги для сравнения.
    
 _cbEntryID2_
  
> [in] Количество вторых идентификаторов записей, указанных параметром _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, используемый в сравнении, который представляет запись адресной книги для сравнения.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на расположение, которое содержит результаты сравнения. 
    

