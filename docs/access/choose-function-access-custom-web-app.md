---
title: Функция Choose (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Возвращает элемент по указанному индексу из списка значений.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282287"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="5154a-103">Функция Choose (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="5154a-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="5154a-104">Возвращает элемент по указанному индексу из списка значений.</span><span class="sxs-lookup"><span data-stu-id="5154a-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5154a-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5154a-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="5154a-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="5154a-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5154a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5154a-107">Syntax</span></span>

<span data-ttu-id="5154a-108">**Нажмите кнопку** (*Индекснумбер*, *значение*, [*валуе_н*])</span><span class="sxs-lookup"><span data-stu-id="5154a-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="5154a-109">Функция **Choose** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="5154a-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="5154a-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="5154a-110">**Argument name**</span></span>|<span data-ttu-id="5154a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5154a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5154a-112">*Индекснумбер*</span><span class="sxs-lookup"><span data-stu-id="5154a-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="5154a-113">Целочисленное выражение, представляющее индекс, отсчитываемый от 1, в списке следующих элементов.</span><span class="sxs-lookup"><span data-stu-id="5154a-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="5154a-114">*Значение*</span><span class="sxs-lookup"><span data-stu-id="5154a-114">*Value*</span></span>  <br/> |<span data-ttu-id="5154a-115">Список значений любого типа данных.</span><span class="sxs-lookup"><span data-stu-id="5154a-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5154a-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5154a-116">Remarks</span></span>

<span data-ttu-id="5154a-117">Если предоставленный *индекснумбер* не является целым числом, значение неявно преобразуется в целое число.</span><span class="sxs-lookup"><span data-stu-id="5154a-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="5154a-118">Если значение индекса превышает границы массива значений, **выберите** возвращает null.</span><span class="sxs-lookup"><span data-stu-id="5154a-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

