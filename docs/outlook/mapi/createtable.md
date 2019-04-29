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
# <a name="createtable"></a><span data-ttu-id="0f417-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="0f417-103">CreateTable</span></span>

  
  
<span data-ttu-id="0f417-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f417-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f417-105">Создает структуры и дескриптор объекта для объекта [итабледата](itabledataiunknown.md) , который можно использовать для создания содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="0f417-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f417-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0f417-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f417-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="0f417-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0f417-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0f417-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f417-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0f417-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0f417-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0f417-110">Called by:</span></span>  <br/> |<span data-ttu-id="0f417-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="0f417-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="0f417-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f417-112">Parameters</span></span>

 <span data-ttu-id="0f417-113">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="0f417-113">_lpInterface_</span></span>
  
> <span data-ttu-id="0f417-114">возврата Указатель на идентификатор интерфейса (IID) для объекта данных TABLE.</span><span class="sxs-lookup"><span data-stu-id="0f417-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="0f417-115">Допустимый идентификатор интерфейса — Иид_имапитабледата.</span><span class="sxs-lookup"><span data-stu-id="0f417-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="0f417-116">При передаче значения NULL в параметре _лпинтерфаце_ объект табличных данных, возвращаемый в параметре _лпптабледата_ , будет приведен к стандартному интерфейсу для объекта данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="0f417-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="0f417-117">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="0f417-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="0f417-118">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="0f417-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="0f417-119">_Лпаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="0f417-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="0f417-120">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="0f417-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="0f417-121">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="0f417-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="0f417-122">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="0f417-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="0f417-123">_Лпвресервед_</span><span class="sxs-lookup"><span data-stu-id="0f417-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="0f417-124">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="0f417-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="0f417-125">_Ултаблетипе_</span><span class="sxs-lookup"><span data-stu-id="0f417-125">_ulTableType_</span></span>
  
> <span data-ttu-id="0f417-126">возврата Тип таблицы, доступный клиентскому приложению или поставщику услуг в составе данных, возвращаемых с помощью [IMAPITable::-Status](imapitable-getstatus.md) , в представлениях таблицы.</span><span class="sxs-lookup"><span data-stu-id="0f417-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="0f417-127">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="0f417-127">Possible values are:</span></span> 
    
<span data-ttu-id="0f417-128">ТБЛТИПЕ_ДИНАМИК</span><span class="sxs-lookup"><span data-stu-id="0f417-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="0f417-129">Содержимое таблицы является динамическим и может изменяться при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="0f417-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="0f417-130">ТБЛТИПЕ_КЭЙСЕТ</span><span class="sxs-lookup"><span data-stu-id="0f417-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="0f417-131">Строки в таблице фиксированы, но значения в этих строках являются динамическими и могут изменяться при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="0f417-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="0f417-132">ТБЛТИПЕ_СНАПШОТ</span><span class="sxs-lookup"><span data-stu-id="0f417-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="0f417-133">Таблица является статической, и ее содержимое не изменяется при изменении базовых данных.</span><span class="sxs-lookup"><span data-stu-id="0f417-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="0f417-134">_Улпроптагиндексколумн_</span><span class="sxs-lookup"><span data-stu-id="0f417-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="0f417-135">возврата Номер индекса столбца, используемый при изменении табличных данных.</span><span class="sxs-lookup"><span data-stu-id="0f417-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="0f417-136">_Лпспроптагаррайколумнс_</span><span class="sxs-lookup"><span data-stu-id="0f417-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="0f417-137">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств, указывающих свойства, необходимые в таблице, для которой объект содержит данные.</span><span class="sxs-lookup"><span data-stu-id="0f417-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="0f417-138">_Лпптабледата_</span><span class="sxs-lookup"><span data-stu-id="0f417-138">_lppTableData_</span></span>
  
> <span data-ttu-id="0f417-139">вышли Указатель на указатель на возвращенный объект данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="0f417-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f417-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f417-140">Return value</span></span>

<span data-ttu-id="0f417-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f417-141">S_OK</span></span> 
  
> <span data-ttu-id="0f417-142">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0f417-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f417-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f417-143">Remarks</span></span>

<span data-ttu-id="0f417-144">Входные параметры _лпаллокатебуффер_, _лпаллокатеморе_и _Лпфрибуффер_ заменяют функции [мапиаллокатебуффер](mapiallocatebuffer.md), [мапиаллокатеморе](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="0f417-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="0f417-145">Клиентское приложение, вызывающее **креатетабле** , передает указатели на функции MAPI только с именем; поставщик услуг передает указатели на эти функции, полученные в результате инициализации или извлеченные при вызове метода [имаписуппорт:: жетмемаллокраутинес](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="0f417-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f417-146">См. также</span><span class="sxs-lookup"><span data-stu-id="0f417-146">See also</span></span>



[<span data-ttu-id="0f417-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f417-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

