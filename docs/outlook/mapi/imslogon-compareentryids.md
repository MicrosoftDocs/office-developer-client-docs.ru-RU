---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410135"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту. MAPI обращается к поставщику услуг только в том случае, если уникальные идентификаторы (UID) в обоих идентификаторах записей, которые необходимо сравнить, обрабатываются этим поставщиком.
  
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
  
> [in] Размер идентификатора записи в вайтах, на который указывает  параметр _lpEntryID1._
    
 _lpEntryID1_
  
> [in] Указатель на идентификатор первой записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Размер идентификатора записи в вайтах, на который указывает  параметр _lpEntryID2._
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на возвращенный результат сравнения. TRUE, если два идентификатора записей ссылаются на один и тот же объект; в противном случае false.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики store сообщений реализуют метод **IMSLogon::CompareEntryIDs** для сравнения двух идентификаторов записей для заданной записи в хранилище сообщений, чтобы определить, ссылаются ли они на один и тот же объект. Если два идентификатора записей ссылаются на один и тот же объект, **CompareEntryIDs** задает для параметра  _lpulResult_ true; Если они ссылаются на разные объекты, **CompareEntryIDs** устанавливает  _для lpulResult_ false. 
  
 **CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записей. Это может произойти, например, после установки новой версии поставщика store сообщений. 
  
## <a name="see-also"></a>См. также



[IMSLogon : IUnknown](imslogoniunknown.md)

