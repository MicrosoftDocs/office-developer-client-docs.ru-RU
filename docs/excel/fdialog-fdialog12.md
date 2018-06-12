---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- функция fdialog [excel 2007], функция fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807252"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="eb4de-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="eb4de-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="eb4de-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="eb4de-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="eb4de-106">Пример пользовательской команды, демонстрируется создание UDD Excel Microsoft (пользовательские диалоговое окно "") в библиотеке DLL с помощью возможностей поле диалогового окна в C API.</span><span class="sxs-lookup"><span data-stu-id="eb4de-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="eb4de-107">При загрузке GENERIC.xll, он создает пользовательских меню, общая, через который доступ к этой команды.</span><span class="sxs-lookup"><span data-stu-id="eb4de-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="eb4de-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="eb4de-108">Parameters</span></span>

<span data-ttu-id="eb4de-109">Функция не принимает параметры.</span><span class="sxs-lookup"><span data-stu-id="eb4de-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="eb4de-110">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb4de-110">Property value/Return value</span></span>

<span data-ttu-id="eb4de-111">Функция всегда возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="eb4de-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="eb4de-112">Пример</span><span class="sxs-lookup"><span data-stu-id="eb4de-112">Example</span></span>

<span data-ttu-id="eb4de-113">Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции.</span><span class="sxs-lookup"><span data-stu-id="eb4de-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb4de-114">См. также</span><span class="sxs-lookup"><span data-stu-id="eb4de-114">See also</span></span>



[<span data-ttu-id="eb4de-115">В универсальные библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="eb4de-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

