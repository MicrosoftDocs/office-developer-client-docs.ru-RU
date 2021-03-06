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
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424261"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записей, принадлежащих конкретному поставщику адресной книги, чтобы определить, относятся ли они к одному объекту адресной книги. 
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID1_
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [вышел] Указатель на результат сравнения. Содержимое  _lpulResult_ настроено на TRUE, если два идентификатора записи ссылаются на один и тот же объект; в противном случае содержимое настроено на FALSE. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Один или оба идентификатора записи, переданных с  _параметрами lpEntryID1_ или  _lpEntryID2,_ не распознаются ни одним поставщиком адресной книги. 
    
## <a name="remarks"></a>Примечания

Клиентские приложения и поставщики услуг называют метод **CompareEntryIDs** для сравнения двух идентификаторов записей, принадлежащих одному поставщику адресной книги, чтобы определить, относятся ли они к одному объекту. **CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записи. Такая ситуация может возникнуть, например, после установки новой версии поставщика адресной книги. 
  
MAPI передает этот вызов поставщику адресной книги, который отвечает за идентификаторы записей, определяя соответствующего поставщика, соединая структуру [MAPIUID](mapiuid.md) в идентификаторах записи со структурой **MAPIUID,** зарегистрированной поставщиком. 
  
Если два идентификатора записи ссылаются на один и тот же объект, **CompareEntryIDs** задает содержимое  _параметра lpulResult_ к TRUE; Если они ссылаются на различные объекты, **compareEntryIDs** задает содержимое false. В любом случае **compareEntryID возвращает** S_OK. Если **compareEntryIDs** возвращает ошибку, которая может возникнуть, если ни один поставщик адресной книги не зарегистрировал структуру **MAPIUID,** которая соответствует одной из идентификаторов записи, клиенты и поставщики не должны принимать никаких действий на основе результатов сравнения. Вместо этого они должны использовать наиболее консервативный подход к выполняемому действию. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

