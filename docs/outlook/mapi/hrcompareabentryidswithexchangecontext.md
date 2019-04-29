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
  
Безопасно сравнивает две адресные книги **идентификаторами EntryID** в нескольких профилях Exchange. Эта функция является функцией замены для [IAddrBook:: метод compareentryids](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |абхелп. h  <br/> |
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

 _пмсесс_
  
> возврата Вошедший в систему **IMAPISession**. Он не может иметь значение NULL.
    
 _Пемсмдбуид_
  
> возврата Указатель на **емсмдбуид** , определяющий службу Exchange, которая содержит поставщика адресных книг Exchange, которую эта функция должна использовать для отображения сведений об идентификаторе записи. Если входящий идентификатор записи не является идентификатором записи поставщика адресных книг Exchange, этот параметр игнорируется, а вызов функции работает так же, как [IAddrBook::D етаилс](iaddrbook-details.md). Если этот параметр имеет значение NULL или нулевой МАПИУИД, эта функция ведет себя так же, как [IAddrBook::D етаилс](iaddrbook-details.md).
    
 _Паддрбук_
  
> возврата Адресная книга, используемая для открытия идентификатора записи. Он не может иметь значение NULL.
    
 _cbEntryID1_
  
> возврата Число байтов первого идентификатора записи, заданного параметром _lpEntryID1_ . 
    
 _lpEntryID1_
  
> возврата Указатель на первый идентификатор записи, представляющий запись адресной книги для сравнения.
    
 _cbEntryID2_
  
> возврата Число байтов второго идентификатора записи, заданного параметром _lpEntryID2_ . 
    
 _lpEntryID2_
  
> возврата Указатель на второй идентификатор записи, используемый в сравнении, представляющем запись адресной книги для сравнения.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лпулресулт_
  
> вышли Указатель на расположение, в котором содержатся результаты сравнения. 
    

