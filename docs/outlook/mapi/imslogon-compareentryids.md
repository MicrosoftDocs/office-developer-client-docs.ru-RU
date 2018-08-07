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
ms.openlocfilehash: c2e6600af66f3dab8ff0fbb5442a1354687a3cbb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809415"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Относится к**: Outlook 
  
Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект. MAPI ссылается этот вызов к поставщику услуг только в том случае, если уникальных идентификаторов (UID) в обоих идентификаторы записей для сравнения обрабатываются этого поставщика.
  
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
  
> [in] Указывает размер в байтах, идентификатор записи с помощью параметра _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Указатель на первый идентификатор записи для сравнения.
    
 _cbEntryID2_
  
> [in] Указывает размер в байтах, идентификатор записи с помощью параметра _lpEntryID2_ _._
    
 _lpEntryID2_
  
> [in] Указатель на второй идентификатор записи для сравнения.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpulResult_
  
> [out] Указатель на возвращаемый результат сравнения. Значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Поставщики хранилища сообщений реализуйте метод **IMSLogon::CompareEntryIDs** для сравнения двух идентификаторов запись соответствующей записи в хранилище сообщений, чтобы определить, является ли они ссылаются на тот же объект. Если идентификаторы двух записей ссылаются на тот же объект, **CompareEntryIDs** параметру _lpulResult_ присваивается значение TRUE; Если они ссылаются на разных объектов, **CompareEntryIDs** задает _lpulResult_ значение FALSE. 
  
 **CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей. Это может произойти, например, после установки новой версии поставщика хранилища сообщений. 
  
## <a name="see-also"></a>См. также



[IMSLogon : IUnknown](imslogoniunknown.md)

