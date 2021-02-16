---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- Функция xloper12toxloper [excel 2007]
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
# <a name="xloper12toxloper"></a><span data-ttu-id="0c938-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="0c938-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="0c938-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0c938-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0c938-106">Процедура преобразования, используемая для преобразования из **нового XLOPER12** в старый **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="0c938-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="0c938-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c938-107">Parameters</span></span>

<span data-ttu-id="0c938-108">_pxloper12_ (**LPXLOPER12)**</span><span class="sxs-lookup"><span data-stu-id="0c938-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="0c938-109">Указатель на исходный **XLOPER12 для** преобразования.</span><span class="sxs-lookup"><span data-stu-id="0c938-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="0c938-110">_pxloper_ (**LPXLOPER)**</span><span class="sxs-lookup"><span data-stu-id="0c938-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="0c938-111">Указатель на целевой **объект XLOPER,** содержащий преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="0c938-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0c938-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c938-112">Property value/Return value</span></span>

<span data-ttu-id="0c938-113">**TRUE,** если преобразование успешно, в противном случае **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="0c938-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0c938-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c938-114">Remarks</span></span>

<span data-ttu-id="0c938-115">В зависимости от типа **XLOPER12** эта функция выделяет новый буфер памяти для преобразованных значений, на которые указывают целевые **значения XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="0c938-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="0c938-116">Если преобразование успешно, вызываемая отвечает за освободить память, связанную с копией; **FreeXLOperT** можно использовать или сделать это напрямую с помощью **бесплатного .**</span><span class="sxs-lookup"><span data-stu-id="0c938-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="0c938-117">Если преобразование не удается, вызываемой не требуется освободить память.</span><span class="sxs-lookup"><span data-stu-id="0c938-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="0c938-118">Преобразование **из XLOPER12** в **XLOPER** может привести к сбою, если **XLOPER12** содержит слишком большой массив или ссылку или слишком длинную строку для **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="0c938-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="0c938-119">**XLOPER12** Строки юникода с широкими символами преобразуются в строки byte **XLOPER** ASCII в зависимости от региональных стандартов.</span><span class="sxs-lookup"><span data-stu-id="0c938-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="0c938-120">**XLOPER12** **xltypeInt** — это 32-битное подписанное integer, а **XLOPER** **xltypeInt** — 16-битное подписанное.</span><span class="sxs-lookup"><span data-stu-id="0c938-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="0c938-121">Если предоставленное **integer XLOPER12** превышает ограничение, задаваемого в виде integer **XLOPER,** это количество преобразуется в 8-byte double и возвращается в **XLOPER** типа **xltypeNum.**</span><span class="sxs-lookup"><span data-stu-id="0c938-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="0c938-122">Это единственный случай, в котором эта функция изменяет тип преобразованной **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="0c938-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="0c938-123">Пример</span><span class="sxs-lookup"><span data-stu-id="0c938-123">Example</span></span>

<span data-ttu-id="0c938-124">Код этой  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` функции см. в файле.</span><span class="sxs-lookup"><span data-stu-id="0c938-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c938-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0c938-125">See also</span></span>

- [<span data-ttu-id="0c938-126">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="0c938-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

