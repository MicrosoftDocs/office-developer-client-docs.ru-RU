---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- функция xloper12toxloper [Excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422910"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="0d76c-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="0d76c-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="0d76c-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0d76c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0d76c-106">Процедура преобразования, используемая для преобразования из **нового XLOPER12** в старый **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="0d76c-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="0d76c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0d76c-107">Parameters</span></span>

<span data-ttu-id="0d76c-108">_pxloper12_ **(LPXLOPER12)**</span><span class="sxs-lookup"><span data-stu-id="0d76c-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="0d76c-109">Указатель на исходный **XLOPER12** для преобразования.</span><span class="sxs-lookup"><span data-stu-id="0d76c-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="0d76c-110">_pxloper_ **(LPXLOPER)**</span><span class="sxs-lookup"><span data-stu-id="0d76c-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="0d76c-111">Указатель на целевой **XLOPER,** чтобы содержать преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="0d76c-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0d76c-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d76c-112">Property value/Return value</span></span>

<span data-ttu-id="0d76c-113">**TRUE,** если преобразование удалось, **FALSE** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0d76c-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0d76c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d76c-114">Remarks</span></span>

<span data-ttu-id="0d76c-115">В зависимости от типа **XLOPER12** эта функция выделяет новый буфер памяти для преобразованных значений, которые указываются в целевом **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="0d76c-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="0d76c-116">Вызывающий отвечает за то, чтобы освободить любую память, связанную с копией, если преобразование успешно; **FreeXLOperT** можно использовать или сделать это напрямую с помощью **бесплатного**.</span><span class="sxs-lookup"><span data-stu-id="0d76c-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="0d76c-117">Если преобразование не удается, вызываемой не требуется освободить память.</span><span class="sxs-lookup"><span data-stu-id="0d76c-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="0d76c-118">Преобразование **из XLOPER12** в **XLOPER** может привести к сбою, если **XLOPER12** содержит слишком большой массив или ссылку, слишком длинную для **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="0d76c-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="0d76c-119">**XLOPER12** Строки с широкими символами юникода преобразуются в строки **byte XLOPER** ASCII, зависящие от локальности.</span><span class="sxs-lookup"><span data-stu-id="0d76c-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="0d76c-120">**XLOPER12** **xltypeInt** — это 32-битный подписанный ряд, в то время как **xltypeInt** **XLOPER** — это 16-битный подписанный ряд.</span><span class="sxs-lookup"><span data-stu-id="0d76c-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="0d76c-121">Если количество комплектуемого **XLOPER12** превышает предельный уровень количества **XLOPER,** он преобразуется в двухместный 8-кет и возвращается в **XLOPER** типа **xltypeNum.**</span><span class="sxs-lookup"><span data-stu-id="0d76c-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="0d76c-122">Это единственный случай, когда эта функция изменяет тип преобразованного **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="0d76c-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="0d76c-123">Пример</span><span class="sxs-lookup"><span data-stu-id="0d76c-123">Example</span></span>

<span data-ttu-id="0d76c-124">См.  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` файл кода для этой функции.</span><span class="sxs-lookup"><span data-stu-id="0d76c-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d76c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0d76c-125">See also</span></span>

- [<span data-ttu-id="0d76c-126">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="0d76c-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

