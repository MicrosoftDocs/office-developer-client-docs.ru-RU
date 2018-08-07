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
ms.openlocfilehash: 24718c50d02da5d60a6594f56ea6100650fe9f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809125"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="153a8-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="153a8-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="153a8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="153a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="153a8-105">Изменяет состояние таблицы путем добавления строки или изменение существующей строки.</span><span class="sxs-lookup"><span data-stu-id="153a8-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="153a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="153a8-106">Parameters</span></span>

 <span data-ttu-id="153a8-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="153a8-107">_cValues_</span></span>
  
> <span data-ttu-id="153a8-108">[in] Число свойств, включаемых в строку новое или измененное состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="153a8-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="153a8-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="153a8-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="153a8-110">[in] Указатель на массив значений свойств, которые описывают свойства в качестве столбцов в строке состояния новые или измененные таблицы.</span><span class="sxs-lookup"><span data-stu-id="153a8-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="153a8-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="153a8-111">_ulFlags_</span></span>
  
> <span data-ttu-id="153a8-112">[in] Битовая маска флаги, определяющее порядок обработки информации, которая определяет строку в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="153a8-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="153a8-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="153a8-113">The following flag can be set:</span></span>
    
<span data-ttu-id="153a8-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="153a8-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="153a8-115">Направляет MAPI для объединения свойств, включенных в массиве, на который указывает _lpColumnVals_ с существующей строки в таблице состояния, а не в новую строку.</span><span class="sxs-lookup"><span data-stu-id="153a8-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="153a8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="153a8-117">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="153a8-117">S_OK</span></span> 
  
> <span data-ttu-id="153a8-118">В таблице состояния обновлен успешно.</span><span class="sxs-lookup"><span data-stu-id="153a8-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="153a8-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="153a8-119">Remarks</span></span>

<span data-ttu-id="153a8-120">Метод **IMAPISupport::ModifyStatusRow** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="153a8-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="153a8-121">Поставщики услуг вызвать **ModifyStatusRow** во время входа в систему для добавления строки в таблице состояния и в других случаях во время сеанса для обновления строки.</span><span class="sxs-lookup"><span data-stu-id="153a8-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="153a8-122">**ModifyStatusRow** предоставляет сведения, необходимые для создания таблицы состояния MAPI.</span><span class="sxs-lookup"><span data-stu-id="153a8-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="153a8-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="153a8-123">Notes to callers</span></span>

<span data-ttu-id="153a8-124">Установите флаг STATUSROW_UPDATE при вызове **ModifyStatusRow** вносить изменения свойств в вашей существующей строки в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="153a8-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="153a8-125">Это информирует MAPI передачи только изменяемый столбцы с помощью параметра _lpColumnVals_ .</span><span class="sxs-lookup"><span data-stu-id="153a8-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="153a8-126">Клиенты могут использовать сведения в таблице состояния для доступа к объекту ваше состояние.</span><span class="sxs-lookup"><span data-stu-id="153a8-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="153a8-127">Полный список столбцов, которые необходимо включить в ваше состояние строки в таблице [Состояния](status-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="153a8-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="153a8-128">См. также</span><span class="sxs-lookup"><span data-stu-id="153a8-128">See also</span></span>



[<span data-ttu-id="153a8-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="153a8-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

