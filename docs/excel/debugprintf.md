---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- Функция дебугпринтф [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311006"
---
# <a name="debugprintf"></a><span data-ttu-id="81086-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="81086-104">debugPrintf</span></span>

<span data-ttu-id="81086-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="81086-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="81086-106">Функция библиотеки Framework, которая записывает строку байтов с завершающим нулем в активный отладчик с помощью функции **аутпутдебугстринга**в пакете Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="81086-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="81086-107">Если у приложения нет отладчика, системный отладчик отображает строку.</span><span class="sxs-lookup"><span data-stu-id="81086-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="81086-108">Если приложение не имеет отладчика, а системный отладчик неактивен, **дебугпринтф** не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="81086-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="81086-109">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="81086-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="81086-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="81086-110">Parameters</span></span>

 <span data-ttu-id="81086-111">_Лпформат (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="81086-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="81086-112">Строка формата, которая следует за синтаксисом и правилами, используемыми в функции **спринтф** .</span><span class="sxs-lookup"><span data-stu-id="81086-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="81086-113">_указаны_</span><span class="sxs-lookup"><span data-stu-id="81086-113">_arguments_</span></span>
  
<span data-ttu-id="81086-114">Ноль или более аргументов, которые должны сопоставлять строку формата.</span><span class="sxs-lookup"><span data-stu-id="81086-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="81086-115">Пример</span><span class="sxs-lookup"><span data-stu-id="81086-115">Example</span></span>

<span data-ttu-id="81086-116">Эта функция печатает строку, чтобы показать, что элемент управления был передан.</span><span class="sxs-lookup"><span data-stu-id="81086-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="81086-117">Перед компиляцией необходимо определить флаг _DEBUG, иначе эта функция не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="81086-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="81086-118">См. также</span><span class="sxs-lookup"><span data-stu-id="81086-118">See also</span></span>



[<span data-ttu-id="81086-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="81086-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

