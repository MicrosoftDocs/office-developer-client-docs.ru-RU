---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- функция xlautoadd [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807333"
---
# <a name="xlautoadd"></a><span data-ttu-id="6a2c9-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="6a2c9-104">xlAutoAdd</span></span>

 <span data-ttu-id="6a2c9-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6a2c9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6a2c9-106">Когда пользователь активирует XLL во время сеанса обмена Excel с помощью диспетчера надстроек, добавляемые в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="6a2c9-107">Эта функция не вызывается при запуске и загрузка предварительно установленные надстройки Excel.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="6a2c9-108">Эта функция может использоваться для отображения настраиваемого диалогового окна, о том, что надстройка была активирована, чтение или запись в реестр или проверьте сведения о лицензировании, например.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="6a2c9-109">Excel не требуется XLL внедрение и экспорт этой функции.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="6a2c9-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="6a2c9-110">Parameters</span></span>

<span data-ttu-id="6a2c9-111">Эта функция не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6a2c9-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a2c9-112">Property value/Return value</span></span>

<span data-ttu-id="6a2c9-113">Реализация этой функции должен возвращать 1.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="6a2c9-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="6a2c9-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a2c9-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a2c9-115">Remarks</span></span>

<span data-ttu-id="6a2c9-116">Использование этой функции, что-то, что ваше XLL необходимо сделать при добавлении, диспетчер надстроек.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="6a2c9-117">Пример</span><span class="sxs-lookup"><span data-stu-id="6a2c9-117">Example</span></span>

<span data-ttu-id="6a2c9-118">Просмотреть `\SAMPLES\EXAMPLE\EXAMPLE.C` и `\SAMPLES\GENERIC\GENERIC.C` для примера реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="6a2c9-119">Следующий код является из `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="6a2c9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="6a2c9-120">See also</span></span>



[<span data-ttu-id="6a2c9-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="6a2c9-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="6a2c9-122">Диспетчер надстроек и функции XLL интерфейса</span><span class="sxs-lookup"><span data-stu-id="6a2c9-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

