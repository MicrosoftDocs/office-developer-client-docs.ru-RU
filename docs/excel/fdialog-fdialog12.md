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
- Функция фдиалог [Excel 2007], функция fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304069"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="b4039-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="b4039-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="b4039-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b4039-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b4039-106">Пример пользовательской команды, в которой показано, как создать УДД Microsoft Excel (пользовательское диалоговое окно) в библиотеке DLL с помощью возможностей диалогового окна в API C.</span><span class="sxs-lookup"><span data-stu-id="b4039-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="b4039-107">При загрузке GENERIC. XLL создается пользовательское меню с общим доступом, через которое осуществляется доступ к этой команде.</span><span class="sxs-lookup"><span data-stu-id="b4039-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="b4039-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4039-108">Parameters</span></span>

<span data-ttu-id="b4039-109">Функция не принимает параметры.</span><span class="sxs-lookup"><span data-stu-id="b4039-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b4039-110">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4039-110">Property value/Return value</span></span>

<span data-ttu-id="b4039-111">Функция всегда возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="b4039-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="b4039-112">Пример</span><span class="sxs-lookup"><span data-stu-id="b4039-112">Example</span></span>

<span data-ttu-id="b4039-113">Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе.</span><span class="sxs-lookup"><span data-stu-id="b4039-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4039-114">См. также</span><span class="sxs-lookup"><span data-stu-id="b4039-114">See also</span></span>



[<span data-ttu-id="b4039-115">Функции в универсальной библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="b4039-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

