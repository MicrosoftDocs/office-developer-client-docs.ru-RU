---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406810"
---
# <a name="createiprop"></a>CreateIProp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает объект данных свойства, то есть [объект IPropData.](ipropdataimapiprop.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a>Параметры

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта данных свойства. Допустимым идентификатором интерфейса является IID_IMAPIPropData. При передаче NULL в параметр  _lpInterface_ объект данных свойства, возвращенный в параметре  _lppPropData,_ также приводится к стандартному интерфейсу для объекта данных свойства. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
 _lpvReserved_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _lppPropData_
  
> [out] Указатель на указатель на возвращенный объект данных свойства.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Запрашиваемая поддержка интерфейса для этого объекта не поддерживается.
    
## <a name="remarks"></a>Примечания

Входные параметры  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ указывают на функции [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) соответственно. Клиентская приложение, **вызываемая CreateIProp,** передает указатели только что именовамым функциям MAPI; поставщик услуг передает указатели на эти функции, полученные в вызове инициализации или полученные с помощью вызова метода [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md) 
  

