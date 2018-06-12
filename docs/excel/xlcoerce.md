---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- функция xlCoerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807353"
---
# <a name="xlcoerce"></a><span data-ttu-id="ca612-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="ca612-104">xlCoerce</span></span>

 <span data-ttu-id="ca612-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ca612-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ca612-106">Преобразует один тип **XLOPER**/ **XLOPER12** в другую или ищет значений ячеек на листе.</span><span class="sxs-lookup"><span data-stu-id="ca612-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="ca612-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca612-107">Parameters</span></span>

 <span data-ttu-id="ca612-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="ca612-108">_pxSource_</span></span>
  
<span data-ttu-id="ca612-109">Источник **XLOPER**/ **XLOPER12** , которую требуется преобразовать.</span><span class="sxs-lookup"><span data-stu-id="ca612-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="ca612-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="ca612-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="ca612-111">(Необязательно).</span><span class="sxs-lookup"><span data-stu-id="ca612-111">(Optional).</span></span> <span data-ttu-id="ca612-112">Битовая маска итоговый типов вы готовы для приема.</span><span class="sxs-lookup"><span data-stu-id="ca612-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="ca612-113">Чтобы указать несколько возможных типов следует использовать битовый оператор **или** (|).</span><span class="sxs-lookup"><span data-stu-id="ca612-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="ca612-114">Если этот аргумент задан, ссылки на одну ячейку преобразуются в один из типов значение **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (если ссылка на ячейку пуст) и ссылки на блоки ячеек преобразуются в **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="ca612-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="ca612-115">Это делает **xlCoerce** самый удобный способ поиска значений ячеек.</span><span class="sxs-lookup"><span data-stu-id="ca612-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ca612-116">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca612-116">Property value/Return value</span></span>

<span data-ttu-id="ca612-117">Возвращает приведенное значение (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**или **xltypeMulti**).</span><span class="sxs-lookup"><span data-stu-id="ca612-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca612-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca612-118">Remarks</span></span>

 <span data-ttu-id="ca612-119">**xlCoerce** невозможно преобразовать в или из **xltypeBigData** или **xltypeFlow**.</span><span class="sxs-lookup"><span data-stu-id="ca612-119">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**.</span></span> <span data-ttu-id="ca612-120">Передача типа **xltypeMissing** или **xltypeNil** в качестве _pxDestType_ эквивалентно пропуска аргумента.</span><span class="sxs-lookup"><span data-stu-id="ca612-120">Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument.</span></span> <span data-ttu-id="ca612-121">Преобразование может не работать в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="ca612-121">Conversion can fail in some cases.</span></span> <span data-ttu-id="ca612-122">Например некоторые строки невозможно преобразовать на номера, в то время как другие пользователи могут.</span><span class="sxs-lookup"><span data-stu-id="ca612-122">For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="ca612-123">Если массив или ссылка на ячейку несколькими преобразуется в тип одного значения, результатом является значение элемента верхней левой ячейки или массива.</span><span class="sxs-lookup"><span data-stu-id="ca612-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="ca612-124">Пример</span><span class="sxs-lookup"><span data-stu-id="ca612-124">Example</span></span>

<span data-ttu-id="ca612-125">Следующий код можно найти в `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="ca612-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ca612-126">Функция **xlcAlert** неявно пытается преобразовать аргумента в строку, чтобы шаг приведения, показанный фактически удаляется, а **xInt** может быть передан непосредственно к **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="ca612-126">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**.</span></span> <span data-ttu-id="ca612-127">Как и **xlcAlert** команда макрос, этот код только работает правильно при вызове из листа макросов.</span><span class="sxs-lookup"><span data-stu-id="ca612-127">As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ca612-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ca612-128">See also</span></span>



[<span data-ttu-id="ca612-129">функция xlSet</span><span class="sxs-lookup"><span data-stu-id="ca612-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="ca612-130">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="ca612-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

