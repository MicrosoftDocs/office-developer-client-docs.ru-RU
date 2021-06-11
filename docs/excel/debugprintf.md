---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- функция debugprintf [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424800"
---
# <a name="debugprintf"></a><span data-ttu-id="0a7d7-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="0a7d7-104">debugPrintf</span></span>

<span data-ttu-id="0a7d7-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0a7d7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0a7d7-106">Функция библиотеки framework, которая записывает на активный Windows отладчик с помощью функции SDK **OutputDebugStringA** функцию Null-terminated byte-string для активного отладки.</span><span class="sxs-lookup"><span data-stu-id="0a7d7-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="0a7d7-107">Если в приложении нет отладки, отладка системы отображает строку.</span><span class="sxs-lookup"><span data-stu-id="0a7d7-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="0a7d7-108">Если приложение не имеет отладки и отладка системы не активна, **отладкаPrintf** ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="0a7d7-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="0a7d7-109">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0a7d7-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="0a7d7-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="0a7d7-110">Parameters</span></span>

 <span data-ttu-id="0a7d7-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="0a7d7-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="0a7d7-112">Строка формата, которая следует синтаксисам и правилам, используемым с функцией **sprintf.**</span><span class="sxs-lookup"><span data-stu-id="0a7d7-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="0a7d7-113">_аргументы_</span><span class="sxs-lookup"><span data-stu-id="0a7d7-113">_arguments_</span></span>
  
<span data-ttu-id="0a7d7-114">Ноль или несколько аргументов, чтобы соответствовать строке формата.</span><span class="sxs-lookup"><span data-stu-id="0a7d7-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="0a7d7-115">Пример</span><span class="sxs-lookup"><span data-stu-id="0a7d7-115">Example</span></span>

<span data-ttu-id="0a7d7-116">Эта функция печатает строку, чтобы показать, что управление было передано ему.</span><span class="sxs-lookup"><span data-stu-id="0a7d7-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="0a7d7-117">Флаг _DEBUG должен быть определен перед компиляторией, иначе эта функция ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="0a7d7-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="0a7d7-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0a7d7-118">See also</span></span>



[<span data-ttu-id="0a7d7-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="0a7d7-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

