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
  
Создает объект данных свойства, то есть объект [ипропдата](ipropdataimapiprop.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
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

 _лпинтерфаце_
  
> возврата Указатель на идентификатор интерфейса (IID) для объекта данных свойства. Допустимый идентификатор интерфейса — IID_IMAPIPropData. При передаче значения NULL в параметре _лпинтерфаце_ объект данных свойства, возвращаемый в параметре _лпппропдата_ , будет приведен к стандартному интерфейсу для объекта данных свойства. 
    
 _лпаллокатебуффер_
  
> возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти. 
    
 _лпаллокатеморе_
  
> возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти. 
    
 _лпфрибуффер_
  
> возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти. 
    
 _лпвресервед_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _лпппропдата_
  
> вышли Указатель на указатель на объект данных возвращаемого свойства.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Запрошенный интерфейс не поддерживается для этого объекта.
    
## <a name="remarks"></a>Примечания

Входные параметры _лпаллокатебуффер_, _лпаллокатеморе_и _Лпфрибуффер_ заменяют функции [мапиаллокатебуффер](mapiallocatebuffer.md), [мапиаллокатеморе](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) соответственно. Клиентское приложение, вызывающее **креатеипроп** , передает указатели на функции MAPI только с именем; поставщик услуг передает указатели на эти функции, которые она получала при вызове инициализации, или извлекаются с помощью вызова метода [имаписуппорт:: жетмемаллокраутинес](imapisupport-getmemallocroutines.md) . 
  

