---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438374"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID1_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Указатель на идентификатор первой записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulRet_
  
> [out] Указатель на результат сравнения. TRUE указывает, что два идентификатора записей ссылаются на один и тот же объект; в противном случае false.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификаторы записей успешно сравнены.
    
MAPI_E_INVALID_ENTRYID 
  
> Один или оба идентификатора записей не принадлежат поставщику адресной книги.
    
## <a name="remarks"></a>Примечания

Поставщики адресных книг реализуют метод **CompareEntryIDs** для сравнения двух идентификаторов записей, чтобы определить, ссылаются ли они на один и тот же объект. 
  
 **CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записей; такая ситуация может возникнуть, например, при сравнении краткосрочного идентификатора записи с долгосрочным идентификатором записи. 
  
Дополнительные сведения о создании идентификаторов записей см. в документе [MAPI Entry Identifiers.](mapi-entry-identifiers.md)
  
## <a name="see-also"></a>См. также



[IABLogon : IUnknown](iablogoniunknown.md)

