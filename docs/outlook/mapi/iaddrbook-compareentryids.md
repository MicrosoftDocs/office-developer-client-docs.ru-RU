---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d6f983e49132e7ab6ea402a8e32bb5ec56d1efba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564852"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнение двух идентификаторы записей, относящихся к конкретной адресной книге, чтобы определить, является ли они ссылаются на один и тот же объект адресной книги. 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID1_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи для сравнения.
    
 _cbEntryID2_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи для сравнения.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на результат сравнения. Содержимое _lpulResult_ присвоено значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае содержимое присвоено значение FALSE. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Одно или оба идентификаторы записей, переданными параметрами _lpEntryID1_ или _lpEntryID2_ не распознается любой поставщик адресной книги. 
    
## <a name="remarks"></a>Замечания

Клиентские приложения и службы поставщиков вызовите метод **CompareEntryIDs** для сравнения двух идентификаторов запись, к которой принадлежит поставщик единого адресной книги для определения, является ли они ссылаются на тот же объект. **CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей. Это может произойти, например, после установки новой версии поставщика адресных книг. 
  
MAPI передает этот вызов для доступа к адресной книге, который несет ответственность за идентификаторы записей определение нужного поставщика, сопоставляя структуры [MAPIUID](mapiuid.md) в идентификаторы записей со структурой **MAPIUID** , зарегистрированные, Поставщик. 
  
Если идентификаторы двух записей ссылаются на тот же объект, **CompareEntryIDs** задает содержимое параметр _lpulResult_ имеет значение TRUE; Если они ссылаются на разных объектов, **CompareEntryIDs** задает содержимое значение FALSE. В любом случае **CompareEntryIDs** возвращает значение S_OK. Если **CompareEntryIDs** возвращает ошибку, которая может возникнуть, если доступа к адресной книге зарегистрировала структура **MAPIUID** , соответствует одному в идентификаторы записей, клиентов и поставщиков не должен выполнять каких-либо действий на основе результатов из сравнение. Вместо этого они должен выполнять самый высокий подход к действие, выполняемое. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

