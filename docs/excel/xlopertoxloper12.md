---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- Функция xlopertoxloper12 [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303908"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="d7fa8-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="d7fa8-104">XLOperToXLOper12</span></span>

<span data-ttu-id="d7fa8-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d7fa8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d7fa8-106">Процедура преобразования, используемая для преобразования старой версии **XLOPER** в новую **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="d7fa8-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="d7fa8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7fa8-107">Parameters</span></span>

<span data-ttu-id="d7fa8-108">_пкслопер_ (**Лпкслопер**)</span><span class="sxs-lookup"><span data-stu-id="d7fa8-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="d7fa8-109">Указатель на исходную **XLOPER** , которую необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="d7fa8-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="d7fa8-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="d7fa8-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="d7fa8-111">Указатель на целевую объект **XLOPER12** , в котором будет содержаться преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="d7fa8-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d7fa8-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7fa8-112">Property value/Return value</span></span>

<span data-ttu-id="d7fa8-113">**Значение true** , если преобразование выполнено успешно, в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="d7fa8-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d7fa8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7fa8-114">Remarks</span></span>

<span data-ttu-id="d7fa8-115">В зависимости от типа **XLOPER**эта функция выделяет новый буфер памяти для преобразованных значений, которые указывают на целевую **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="d7fa8-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="d7fa8-116">Вызывающий абонент отвечает за освобождение памяти, связанной с копией, если преобразование является успешным; **FreeXLOper12T** можно использовать, или он может быть выполнен напрямую с помощью **бесплатной**функции.</span><span class="sxs-lookup"><span data-stu-id="d7fa8-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="d7fa8-117">Если преобразование завершается неудачно, вызывающему объекту не требуется освобождать память.</span><span class="sxs-lookup"><span data-stu-id="d7fa8-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="d7fa8-118">Как правило, можно выполнить преобразование из любой **XLOPER** в **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="d7fa8-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="d7fa8-119">В отличие от этого, преобразование из **XLOPER12** в **XLOPER** может закончиться ошибкой, если **XLOPER12** содержит слишком большой массив или ссылку или слишком длинную строку для хранения в ней. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d7fa8-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="d7fa8-120">**XLOPER** Строки байтов ASCII преобразуются \*\*\*\* в строки двухбайтовых символов Юникода, зависящие от языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="d7fa8-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="d7fa8-121">Пример</span><span class="sxs-lookup"><span data-stu-id="d7fa8-121">Example</span></span>

<span data-ttu-id="d7fa8-122">В этом файле `\SAMPLES\FRAMEWRK\FRAMEWRK.C` содержится код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="d7fa8-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

