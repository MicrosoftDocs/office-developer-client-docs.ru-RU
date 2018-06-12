---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- функция xlopertoxloper12 [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807385"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="e861e-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="e861e-104">XLOperToXLOper12</span></span>

<span data-ttu-id="e861e-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e861e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e861e-106">Процедура преобразования используются для преобразования из старого **XLOPER** новые **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="e861e-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="e861e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e861e-107">Parameters</span></span>

<span data-ttu-id="e861e-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="e861e-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="e861e-109">Указатель на источник **XLOPER** преобразование.</span><span class="sxs-lookup"><span data-stu-id="e861e-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="e861e-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="e861e-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="e861e-111">Указатель на целевой **XLOPER12** наличия преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="e861e-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e861e-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e861e-112">Property value/Return value</span></span>

<span data-ttu-id="e861e-113">**Значение TRUE,** Если преобразование выполнено успешно, **значение FALSE** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e861e-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e861e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e861e-114">Remarks</span></span>

<span data-ttu-id="e861e-115">В зависимости от типа **XLOPER**эта функция выделяет новый буфер памяти для преобразованные значения, которые являются направлена в целевом **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="e861e-115">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**.</span></span> <span data-ttu-id="e861e-116">Вызывающий объект несет ответственность за освобождает память, связанных с копией ли преобразование будет успешно; Можно использовать **FreeXLOper12T** или можно выполнить с помощью **свободного**.</span><span class="sxs-lookup"><span data-stu-id="e861e-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="e861e-117">В случае сбоя преобразования вызывающего освободить память, не требуется.</span><span class="sxs-lookup"><span data-stu-id="e861e-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="e861e-118">В общем случае преобразование из любого **XLOPER** **XLOPER12** невозможно.</span><span class="sxs-lookup"><span data-stu-id="e861e-118">In general, conversion from any **XLOPER** to an **XLOPER12** is possible.</span></span> <span data-ttu-id="e861e-119">С другой стороны преобразование из **XLOPER12** **XLOPER** может завершиться неудачно **XLOPER12** содержит массив или ссылку слишком большого размера или строка, слишком много времени для **XLOPER** для хранения.</span><span class="sxs-lookup"><span data-stu-id="e861e-119">In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="e861e-120">**XLOPER** Строки байтов ASCII преобразуются в строки Юникода **XLOPER12** Юникод, чтобы зависит от языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="e861e-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="e861e-121">Пример</span><span class="sxs-lookup"><span data-stu-id="e861e-121">Example</span></span>

<span data-ttu-id="e861e-122">Просмотрите файл `\SAMPLES\FRAMEWRK\FRAMEWRK.C` код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="e861e-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

