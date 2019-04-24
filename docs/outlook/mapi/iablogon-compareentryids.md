---
title: Иаблогонкомпаринтридс
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279610"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.
  
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
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID1_ . 
    
 _lpEntryID1_
  
> возврата Указатель на первый идентификатор записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID2_ . 
    
 _lpEntryID2_
  
> возврата Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лпулрет_
  
> вышли Указатель на результат сравнения. ЗНАЧЕНИЕ TRUE, чтобы указать, что два идентификатора записи ссылаются на один и тот же объект; в противном случае — FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификаторы записей были успешно сравнены.
    
МАПИ_Е_ИНВАЛИД_ЕНТРИД 
  
> Один или оба идентификатора записи не принадлежат поставщику адресной книги.
    
## <a name="remarks"></a>Замечания

Поставщики адресных книг реализуют метод **метод compareentryids** для сравнения двух идентификаторов записей, чтобы определить, ссылаются ли они на один и тот же объект. 
  
 **Метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записей; Такая ситуация может возникнуть, например, при сравнении краткосрочного идентификатора записи с длинным идентификатором записи. 
  
Дополнительные сведения о создании идентификаторов записей можно узнать в статье [идентификаторы записей MAPI](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>См. также



[IABLogon : IUnknown](iablogoniunknown.md)

