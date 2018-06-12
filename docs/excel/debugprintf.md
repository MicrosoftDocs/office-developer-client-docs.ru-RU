---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- функция debugprintf [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807146"
---
# <a name="debugprintf"></a><span data-ttu-id="bbdbc-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="bbdbc-104">debugPrintf</span></span>

<span data-ttu-id="bbdbc-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bbdbc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bbdbc-106">Функция библиотеки Framework, которая записывает символом null байтов строку активного отладчика с помощью пакета SDK Windows функция **OutputDebugStringA**.</span><span class="sxs-lookup"><span data-stu-id="bbdbc-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="bbdbc-107">Если приложение не отладчик, отладчик система отображает строку.</span><span class="sxs-lookup"><span data-stu-id="bbdbc-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="bbdbc-108">Если приложение имеет отладчик не и отладчик система не активен, **debugPrintf** не имеет никакого эффекта.</span><span class="sxs-lookup"><span data-stu-id="bbdbc-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="bbdbc-109">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bbdbc-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="bbdbc-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="bbdbc-110">Parameters</span></span>

 <span data-ttu-id="bbdbc-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="bbdbc-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="bbdbc-112">Строка формата образом синтаксис и правила, которые используются с **достаточен** .</span><span class="sxs-lookup"><span data-stu-id="bbdbc-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="bbdbc-113">_аргументы_</span><span class="sxs-lookup"><span data-stu-id="bbdbc-113">_arguments_</span></span>
  
<span data-ttu-id="bbdbc-114">Ноль или больше аргументов в соответствии с строку формата.</span><span class="sxs-lookup"><span data-stu-id="bbdbc-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="bbdbc-115">Пример</span><span class="sxs-lookup"><span data-stu-id="bbdbc-115">Example</span></span>

<span data-ttu-id="bbdbc-116">Эта функция печатает строку, которую нужно показать, что элемент управления был передан на него.</span><span class="sxs-lookup"><span data-stu-id="bbdbc-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="bbdbc-117">Перед компиляцией необходимо определить флаг _DEBUG, или же эта функция не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="bbdbc-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="bbdbc-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bbdbc-118">See also</span></span>



[<span data-ttu-id="bbdbc-119">Функции в библиотеке Framework</span><span class="sxs-lookup"><span data-stu-id="bbdbc-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

