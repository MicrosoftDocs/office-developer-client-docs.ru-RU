---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417163"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="d1c94-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="d1c94-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="d1c94-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1c94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1c94-105">Изменяет таблицу состояния, добавляя новую строку или изменяя существующую строку.</span><span class="sxs-lookup"><span data-stu-id="d1c94-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d1c94-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d1c94-106">Parameters</span></span>

 <span data-ttu-id="d1c94-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="d1c94-107">_cValues_</span></span>
  
> <span data-ttu-id="d1c94-108">[in] Количество свойств, которые будут включены в новую или измененную строку таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="d1c94-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="d1c94-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="d1c94-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="d1c94-110">[in] Указатель на массив значений свойств, которые описывают свойства, которые будут включены в качестве столбцов в новой или измененной строке таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="d1c94-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="d1c94-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d1c94-111">_ulFlags_</span></span>
  
> <span data-ttu-id="d1c94-112">[in] Битмаска флагов, которая контролирует обработку сведений, определяемых строкой таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="d1c94-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="d1c94-113">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d1c94-113">The following flag can be set:</span></span>
    
<span data-ttu-id="d1c94-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="d1c94-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="d1c94-115">Направляет MAPI для объединения свойств, включенных в массив, на который указывает  _lpColumnVals,_ с существующей строкой таблицы состояния, а не в новой строке.</span><span class="sxs-lookup"><span data-stu-id="d1c94-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d1c94-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1c94-116">Return value</span></span>

<span data-ttu-id="d1c94-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1c94-117">S_OK</span></span> 
  
> <span data-ttu-id="d1c94-118">Таблица состояния была успешно обновлена.</span><span class="sxs-lookup"><span data-stu-id="d1c94-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1c94-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1c94-119">Remarks</span></span>

<span data-ttu-id="d1c94-120">Метод **IMAPISupport::ModifyStatusRow** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d1c94-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="d1c94-121">Поставщики услуг звонят **в ModifyStatusRow** во время логотипа, чтобы добавить строку в таблицу состояния, а в другое время во время сеанса обновить строку.</span><span class="sxs-lookup"><span data-stu-id="d1c94-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="d1c94-122">**ModifyStatusRow** предоставляет MAPI сведения, необходимые для построения таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="d1c94-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d1c94-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d1c94-123">Notes to callers</span></span>

<span data-ttu-id="d1c94-124">Установите флаг STATUSROW_UPDATE при вызове **ModifyStatusRow,** чтобы внести изменения в свойства существующей строки таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="d1c94-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="d1c94-125">Это информирует MAPI о том, что только измененные столбцы передаются в _параметре lpColumnVals._</span><span class="sxs-lookup"><span data-stu-id="d1c94-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="d1c94-126">Клиенты могут использовать сведения в таблице состояния для доступа к объекту состояния.</span><span class="sxs-lookup"><span data-stu-id="d1c94-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="d1c94-127">Полный список столбцов, которые необходимо включить в строку таблицы состояния, см. [в статье Status Tables.](status-tables.md)</span><span class="sxs-lookup"><span data-stu-id="d1c94-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1c94-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d1c94-128">See also</span></span>



[<span data-ttu-id="d1c94-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1c94-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

