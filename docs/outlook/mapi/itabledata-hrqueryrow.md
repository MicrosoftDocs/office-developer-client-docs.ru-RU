---
title: Итабледатахркуериров
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434769"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="8e53a-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="8e53a-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="8e53a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e53a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e53a-105">Получает строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="8e53a-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="8e53a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e53a-106">Parameters</span></span>

 <span data-ttu-id="8e53a-107">_Лпспропвалуе_</span><span class="sxs-lookup"><span data-stu-id="8e53a-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="8e53a-108">возврата Указатель на структуру значения свойства, которая описывает столбец индекса для извлекаемой строки.</span><span class="sxs-lookup"><span data-stu-id="8e53a-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="8e53a-109">Элемент **улпроптаг** структуры значения свойства должен содержать тот же тег свойства, что и параметр _улпроптагиндексколумн_ , из вызова функции [креатетабле](createtable.md) , которая получает доступ к реализации [итабледата](itabledataiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="8e53a-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="8e53a-110">_Лппсров_</span><span class="sxs-lookup"><span data-stu-id="8e53a-110">_lppSRow_</span></span>
  
> <span data-ttu-id="8e53a-111">вышли Указатель на указатель на извлеченную строку.</span><span class="sxs-lookup"><span data-stu-id="8e53a-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="8e53a-112">_Лпулиров_</span><span class="sxs-lookup"><span data-stu-id="8e53a-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="8e53a-113">[вход, выход] В поле input — допустимый указатель или значение NULL, которое указывает, что никакие сведения не требуется возвращать.</span><span class="sxs-lookup"><span data-stu-id="8e53a-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="8e53a-114">В выходных данных — допустимый указатель, указывающий на номер строки строки, порядковый номер, который определяет положение строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="8e53a-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e53a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e53a-115">Return value</span></span>

<span data-ttu-id="8e53a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e53a-116">S_OK</span></span> 
  
> <span data-ttu-id="8e53a-117">Строка была успешно получена.</span><span class="sxs-lookup"><span data-stu-id="8e53a-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="8e53a-118">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="8e53a-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="8e53a-119">Структура [спропвалуе](spropvalue.md) , на которую указывает _лпспропвалуе_ , не содержит свойство столбца index.</span><span class="sxs-lookup"><span data-stu-id="8e53a-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8e53a-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e53a-120">Remarks</span></span>

<span data-ttu-id="8e53a-121">Метод **итабледата:: хркуериров** извлекает все свойства для строки, содержащей столбец индекса, который соответствует значению столбца индекса, включенному в структуру свойства, на которую указывает _лпспропвалуе_.</span><span class="sxs-lookup"><span data-stu-id="8e53a-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="8e53a-122">**Хркуериров** также возвращает номер строки, если вызывающая сторона запрашивает ее, которая определяет положение строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="8e53a-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="8e53a-123">Так как **хркуериров** не изменяет структуру **спропвалуе** , на которую указывает _лпспропвалуе_, вызывающие объекты должны освобождать структуру при возврате **хркуериров** .</span><span class="sxs-lookup"><span data-stu-id="8e53a-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="8e53a-124">Вызывающие также должны освободить структуру **сров** , содержащую извлеченную строку.</span><span class="sxs-lookup"><span data-stu-id="8e53a-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e53a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8e53a-125">See also</span></span>



[<span data-ttu-id="8e53a-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8e53a-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8e53a-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8e53a-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8e53a-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8e53a-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="8e53a-129">SRow</span><span class="sxs-lookup"><span data-stu-id="8e53a-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8e53a-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e53a-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

