---
title: имслогонкомпаринтридс
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
  
Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект. MAPI указывает этот вызов поставщику услуг, только если уникальные идентификаторы (UID) в обоих идентификаторах записей будут обрабатываться этим поставщиком.
  
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
  
> возврата Размер (в байтах) идентификатора записи, на который указывает параметр _lpEntryID1_ _._
    
 _lpEntryID1_
  
> возврата Указатель на первый идентификатор записи, который необходимо сравнить.
    
 _cbEntryID2_
  
> возврата Размер (в байтах) идентификатора записи, на который указывает параметр _lpEntryID2_ _._
    
 _lpEntryID2_
  
> возврата Указатель на второй идентификатор записи, который необходимо сравнить.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _лпулресулт_
  
> вышли Указатель на возвращаемый результат сравнения. Значение TRUE, если два идентификатора записи ссылаются на один объект; в противном случае — FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики хранилища сообщений реализуют метод **имслогон:: метод compareentryids** для сравнения двух идентификаторов записей для заданной записи в хранилище сообщений, чтобы определить, ссылаются ли они на один и тот же объект. Если два идентификатора записи ссылаются на один и тот же объект, **метод compareentryids** устанавливает для параметра _лпулресулт_ значение true; Если они ссылаются на различные объекты, **метод compareentryids** устанавливает для _лпулресулт_ значение false. 
  
 **Метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записи. Это может произойти, например, после установки новой версии поставщика хранилища сообщений. 
  
## <a name="see-also"></a>См. также



[IMSLogon : IUnknown](imslogoniunknown.md)

