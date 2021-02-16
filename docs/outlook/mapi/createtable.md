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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает структуры и handle объекта [ITableData,](itabledataiunknown.md) который можно использовать для создания содержимого таблицы. 
  
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

## <a name="parameters"></a>Параметры

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта данных таблицы. Допустимым идентификатором интерфейса является IID_IMAPITableData. При передаче NULL в параметр  _lpInterface_ объект данных таблицы, возвращенный в параметре  _lppTableData,_ также приводится к стандартному интерфейсу для объекта данных таблицы. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
 _lpvReserved_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _ulTableType_
  
> [in] Тип таблицы, доступный для клиентского приложения или поставщика услуг в составе [IMAPITable::GetStatus,](imapitable-getstatus.md) возвращает данные в представлениях таблиц. Возможные значения: 
    
TBLTYPE_DYNAMIC 
  
> Содержимое таблицы является динамическим и может изменяться по мере изменения данных. 
    
TBLTYPE_KEYSET 
  
> Строки в таблице являются фиксированными, но значения в этих строках являются динамическими и могут изменяться по мере изменения данных. 
    
TBLTYPE_SNAPSHOT 
  
> Таблица является статической, и ее содержимое не меняется при изменении данных. 
    
 _ulPropTagIndexColumn_
  
> [in] Номер индекса столбца для использования при изменении данных таблицы. 
    
 _lpSPropTagArrayColumns_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, указывающих свойства, необходимые в таблице, для которой объект содержит данные. 
    
 _lppTableData_
  
> [out] Указатель на указатель на возвращенный объект данных таблицы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Входные параметры  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ указывают на функции [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) соответственно. Клиентские приложения, **вызываемые CreateTable** передает указатели только что именуемые функции MAPI; поставщик услуг передает указатели на эти функции, полученные в вызове инициализации или полученные с помощью вызова метода [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md) 
  
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)

