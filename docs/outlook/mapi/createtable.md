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
ms.openlocfilehash: 5d4717dad51e7e6b90da59d285268761eec84d7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564152"
---
# <a name="createtable"></a>CreateTable

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создание структуры и дескриптор объекта для объекта [ITableData](itabledataiunknown.md) , которую можно использовать для создания содержимого таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса) для объекта в таблице данных. Допустимый идентификатор является IID_IMAPITableData. Указать значение NULL для параметра _lpInterface_ вызывает объект данных в таблице, возвращаемой в параметре _lppTableData_ приведения стандартный интерфейс для объекта данных в таблице. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти. 
    
 _lpvReserved_
  
> [in] ���������������; ������ ���� ����� ����. 
    
 _ulTableType_
  
> [in] Тип таблицы, доступные в клиентском приложении или поставщика услуг в составе [IMAPITable::GetStatus](imapitable-getstatus.md) возвращаемые данные в режимах таблицы. Возможные значения: 
    
TBLTYPE_DYNAMIC 
  
> Содержимое таблицы являются динамическими и можно изменить при изменении базовых данных. 
    
TBLTYPE_KEYSET 
  
> Исправленные строки в таблице, но значения в следующих строках динамических и можно изменить при изменении базовых данных. 
    
TBLTYPE_SNAPSHOT 
  
> В таблице приведен статических и содержимое не изменяются при изменении базовых данных. 
    
 _ulPropTagIndexColumn_
  
> [in] Индекс столбца для использования при изменении данных в таблице. 
    
 _lpSPropTagArrayColumns_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив теги свойство, указывающее, свойства, необходимые в таблице, для которого объект содержит данные. 
    
 _lppTableData_
  
> [out] Указатель на указатель на объект возвращаемой таблицы данных.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Входные параметры _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ пункты функции [MAPIFreeBuffer](mapifreebuffer.md) , [MAPIAllocateMore](mapiallocatemore.md)и [MAPIAllocateBuffer](mapiallocatebuffer.md)соответственно. Клиентское приложение вызов **CreateTable** передается в указатели функции MAPI только с именем; Поставщик службы передает указатели эти функции, которые он полученных в его инициализация звонок или получить с помощью вызова метода [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)

