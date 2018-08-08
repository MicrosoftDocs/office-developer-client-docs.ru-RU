---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- функция xloper12toxloper [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807370"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="af341-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="af341-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="af341-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="af341-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="af341-106">Процедура преобразования используются для преобразования из нового **XLOPER12** старый **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="af341-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="af341-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="af341-107">Parameters</span></span>

<span data-ttu-id="af341-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="af341-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="af341-109">Указатель на источник **XLOPER12** преобразование.</span><span class="sxs-lookup"><span data-stu-id="af341-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="af341-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="af341-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="af341-111">Указатель на целевой **XLOPER** наличия преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="af341-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="af341-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af341-112">Property value/Return value</span></span>

<span data-ttu-id="af341-113">**Значение TRUE,** Если преобразование выполнено успешно, **значение FALSE** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="af341-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af341-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="af341-114">Remarks</span></span>

<span data-ttu-id="af341-115">В зависимости от типа **XLOPER12**эта функция выделяет новый буфер памяти для преобразованные значения, которые являются направлена в целевом **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="af341-115">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**.</span></span> <span data-ttu-id="af341-116">Вызывающий объект несет ответственность за освобождает память, связанных с копией ли преобразование будет успешно; Можно использовать **FreeXLOperT** или это можно сделать с помощью **свободного**.</span><span class="sxs-lookup"><span data-stu-id="af341-116">The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="af341-117">В случае сбоя преобразования вызывающего освободить память, не требуется.</span><span class="sxs-lookup"><span data-stu-id="af341-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="af341-118">Преобразование из **XLOPER12** **XLOPER** может завершиться неудачно **XLOPER12** содержит массив или ссылку слишком большого размера или строка, слишком много времени для **XLOPER** для хранения.</span><span class="sxs-lookup"><span data-stu-id="af341-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="af341-119">**XLOPER12** Строки двухбайтовых знаков Юникод преобразуются в строки байтов **XLOPER** ASCII в способом, зависящих от языковых стандартов.</span><span class="sxs-lookup"><span data-stu-id="af341-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="af341-120">**XLOPER12** **xltypeInt** — 32-разрядное целое число со знаком, а **XLOPER** **xltypeInt** — 16-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="af341-120">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer.</span></span> <span data-ttu-id="af341-121">Когда предоставленное целое **XLOPER12** превышает ограничение **XLOPER** целого числа, целое число преобразуется в double 8 байтов и возвращаются в **XLOPER** из типа **xltypeNum**.</span><span class="sxs-lookup"><span data-stu-id="af341-121">When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**.</span></span> <span data-ttu-id="af341-122">Это единственный случай, в котором эта функция изменяет тип преобразованные **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="af341-122">This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="af341-123">Пример</span><span class="sxs-lookup"><span data-stu-id="af341-123">Example</span></span>

<span data-ttu-id="af341-124">Просмотрите файл `\SAMPLES\FRAMEWRK\FRAMEWRK.C` код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="af341-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af341-125">См. также</span><span class="sxs-lookup"><span data-stu-id="af341-125">See also</span></span>

- [<span data-ttu-id="af341-126">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="af341-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

