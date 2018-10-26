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
ms.openlocfilehash: b161c8c0da78b5ca872b87cad9a297169426d4cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565006"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.
  
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
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи для сравнения.
    
 _cbEntryID2_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи для сравнения.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulRet_
  
> [out] Указатель на результат сравнения. Значение TRUE, чтобы указать, что идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификаторы записей было успешно выполнено.
    
MAPI_E_INVALID_ENTRYID 
  
> Одно или оба идентификаторы записей не принадлежат к адресной книге.
    
## <a name="remarks"></a>Замечания

Метод **CompareEntryIDs** для сравнения двух идентификаторы записей для определения, является ли они ссылаются на тот же объект, реализуемые поставщиками адресных книг. 
  
 **CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей; такой ситуации может произойти, например, при сравнении краткосрочных идентификатор записи с долгосрочного идентификатор записи. 
  
Дополнительные сведения о том, как создавать идентификаторы записей можно [Идентификаторы MAPI записей](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>См. также



[IABLogon : IUnknown](iablogoniunknown.md)

