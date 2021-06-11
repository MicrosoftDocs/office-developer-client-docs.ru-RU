---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- функция xlopertoxloper12 [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404598"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="b9243-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="b9243-104">XLOperToXLOper12</span></span>

<span data-ttu-id="b9243-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b9243-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b9243-106">Процедура преобразования, используемая для преобразования из **старого XLOPER** в **новый XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="b9243-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="b9243-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b9243-107">Parameters</span></span>

<span data-ttu-id="b9243-108">_pxloper_ **(LPXLOPER)**</span><span class="sxs-lookup"><span data-stu-id="b9243-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="b9243-109">Указатель на исходный **XLOPER** для преобразования.</span><span class="sxs-lookup"><span data-stu-id="b9243-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="b9243-110">_pxloper12_ **(LPXLOPER12)**</span><span class="sxs-lookup"><span data-stu-id="b9243-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="b9243-111">Указатель на целевое **значение XLOPER12,** чтобы содержать преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="b9243-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b9243-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9243-112">Property value/Return value</span></span>

<span data-ttu-id="b9243-113">**TRUE,** если преобразование удалось, **FALSE** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b9243-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b9243-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9243-114">Remarks</span></span>

<span data-ttu-id="b9243-115">В зависимости от типа **XLOPER** эта функция выделяет новый буфер памяти для преобразованных значений, которые указываются в целевом **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="b9243-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="b9243-116">Вызывающий отвечает за то, чтобы освободить любую память, связанную с копией, если преобразование успешно; **FreeXLOper12T** можно использовать, или это можно сделать непосредственно с помощью **бесплатно**.</span><span class="sxs-lookup"><span data-stu-id="b9243-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="b9243-117">Если преобразование не удается, вызываемой не требуется освободить память.</span><span class="sxs-lookup"><span data-stu-id="b9243-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="b9243-118">Как правило, возможно преобразование **из любого XLOPER** в **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="b9243-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="b9243-119">В отличие от этого, преобразование **из XLOPER12** в **XLOPER** может привести к сбою, если **XLOPER12** содержит слишком большой массив или ссылку, слишком длинную для **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="b9243-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="b9243-120">**XLOPER** Строки byte ASCII преобразуются в строки широкого характера **XLOPER12** Unicode таким образом, что зависят от локальности.</span><span class="sxs-lookup"><span data-stu-id="b9243-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="b9243-121">Пример</span><span class="sxs-lookup"><span data-stu-id="b9243-121">Example</span></span>

<span data-ttu-id="b9243-122">См.  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` файл кода для этой функции.</span><span class="sxs-lookup"><span data-stu-id="b9243-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

