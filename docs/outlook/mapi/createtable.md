---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435014"
---
# <a name="createtable"></a>CreateTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает структуры и ручку объекта для [объекта ITableData,](itabledataiunknown.md) которые можно использовать для создания содержимого таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта данных таблицы. Допустимый идентификатор интерфейса IID_IMAPITableData. Передача NULL в  _параметре lpInterface_ также приводит к возвращению объекта данных таблицы в  _параметре lppTableData_ в стандартный интерфейс для объекта данных таблицы. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти. 
    
 _lpvReserved_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _ulTableType_
  
> [in] Тип таблицы, доступный клиенту или поставщику услуг в составе [данных IMAPITable::GetStatus,](imapitable-getstatus.md) возвращаемых в представлениях таблицы. Возможные значения: 
    
TBLTYPE_DYNAMIC 
  
> Содержимое таблицы динамическое и может изменяться по мере изменения данных. 
    
TBLTYPE_KEYSET 
  
> Строки в таблице фиксируются, но значения в этих строках динамически и могут изменяться по мере изменения данных. 
    
TBLTYPE_SNAPSHOT 
  
> Таблица статична, а содержимое не меняется при изменении данных. 
    
 _ulPropTagIndexColumn_
  
> [in] Индексировать число столбца для использования при изменении данных таблицы. 
    
 _lpSPropTagArrayColumns_
  
> [in] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержащий массив тегов свойств, указывающих свойства, необходимые в таблице, для которой объект содержит данные. 
    
 _lppTableData_
  
> [вышел] Указатель на указатель на возвращенный объект данных таблицы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Параметры  _ввода lpAllocateBuffer_,  _lpAllocateMore_ и  _lpFreeBuffer_ указывают на функции [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) соответственно. Клиентская **заявка, вызываемая CreateTable,** передает указатели на только что названные функции MAPI; поставщик услуг передает указатели на эти функции, полученные в вызове инициализации или полученные с помощью вызова метода [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md) 
  
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)

