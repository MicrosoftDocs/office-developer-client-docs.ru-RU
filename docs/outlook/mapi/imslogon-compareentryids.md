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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту. MAPI передает этот вызов поставщику услуг только в том случае, если уникальные идентификаторы (UID) в обоих идентификаторах записи, которые необходимо сравнить, обрабатываются этим поставщиком.
  
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
  
> [in] Размер в bytes идентификатора записи, на который указывает параметр _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> [in] Размер в bytes идентификатора записи, на который указывает параметр _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [вышел] Указатель на возвращенный результат сравнения. TRUE, если два идентификатора записи относятся к одному объекту; в противном случае FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики магазинов сообщений реализуют метод **IMSLogon::CompareEntryIDs** для сравнения двух идентификаторов записи для данной записи в хранилище сообщений, чтобы определить, относятся ли они к одному объекту. Если два идентификатора записи ссылаются на один и тот же объект, **compareEntryIDs** задает  _параметр lpulResult_ true; Если они ссылаются на различные объекты, **compareEntryIDs** задает  _lpulResult_ false. 
  
 **CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записи. Это может произойти, например, после установки новой версии поставщика магазина сообщений. 
  
## <a name="see-also"></a>См. также



[IMSLogon : IUnknown](imslogoniunknown.md)

