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
ms.openlocfilehash: 5f42e1eb0d120d2fbb785e63b451acdd2d5a91f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808251"
---
# <a name="createtable"></a><span data-ttu-id="ef6f9-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="ef6f9-103">CreateTable</span></span>

  
  
<span data-ttu-id="ef6f9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef6f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef6f9-105">Создание структуры и дескриптор объекта для объекта [ITableData](itabledataiunknown.md) , которую можно использовать для создания содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef6f9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ef6f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="ef6f9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ef6f9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ef6f9-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="ef6f9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ef6f9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ef6f9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ef6f9-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="ef6f9-110">Called by:</span></span>  <br/> |<span data-ttu-id="ef6f9-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="ef6f9-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ef6f9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef6f9-112">Parameters</span></span>

 <span data-ttu-id="ef6f9-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-113">_lpInterface_</span></span>
  
> <span data-ttu-id="ef6f9-114">[in] Указатель на идентификатор интерфейса (ИД интерфейса) для объекта в таблице данных.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="ef6f9-115">Допустимый идентификатор является IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="ef6f9-116">Указать значение NULL для параметра _lpInterface_ вызывает объект данных в таблице, возвращаемой в параметре _lppTableData_ приведения стандартный интерфейс для объекта данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="ef6f9-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="ef6f9-118">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="ef6f9-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="ef6f9-120">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="ef6f9-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="ef6f9-122">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="ef6f9-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="ef6f9-124">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="ef6f9-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-125">_ulTableType_</span></span>
  
> <span data-ttu-id="ef6f9-126">[in] Тип таблицы, доступные в клиентском приложении или поставщика услуг в составе [IMAPITable::GetStatus](imapitable-getstatus.md) возвращаемые данные в режимах таблицы.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="ef6f9-127">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="ef6f9-127">Possible values are:</span></span> 
    
<span data-ttu-id="ef6f9-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="ef6f9-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="ef6f9-129">Содержимое таблицы являются динамическими и можно изменить при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="ef6f9-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="ef6f9-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="ef6f9-131">Исправленные строки в таблице, но значения в следующих строках динамических и можно изменить при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="ef6f9-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="ef6f9-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="ef6f9-133">В таблице приведен статических и содержимое не изменяются при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="ef6f9-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="ef6f9-135">[in] Индекс столбца для использования при изменении данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="ef6f9-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="ef6f9-137">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив теги свойство, указывающее, свойства, необходимые в таблице, для которого объект содержит данные.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="ef6f9-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="ef6f9-138">_lppTableData_</span></span>
  
> <span data-ttu-id="ef6f9-139">[out] Указатель на указатель на объект возвращаемой таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ef6f9-140">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ef6f9-140">Return value</span></span>

<span data-ttu-id="ef6f9-141">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ef6f9-141">S_OK</span></span> 
  
> <span data-ttu-id="ef6f9-142">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef6f9-143">���������</span><span class="sxs-lookup"><span data-stu-id="ef6f9-143">Remarks</span></span>

<span data-ttu-id="ef6f9-144">Входные параметры _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ пункты функции [MAPIFreeBuffer](mapifreebuffer.md) , [MAPIAllocateMore](mapiallocatemore.md)и [MAPIAllocateBuffer](mapiallocatebuffer.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="ef6f9-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="ef6f9-145">Клиентское приложение вызов **CreateTable** передается в указатели функции MAPI только с именем; Поставщик службы передает указатели эти функции, которые он полученных в его инициализация звонок или получить с помощью вызова метода [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="ef6f9-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef6f9-146">См. также</span><span class="sxs-lookup"><span data-stu-id="ef6f9-146">See also</span></span>



[<span data-ttu-id="ef6f9-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef6f9-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

