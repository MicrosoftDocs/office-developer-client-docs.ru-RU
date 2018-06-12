---
title: Последовательно выберите пункты функции (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Возвращает элемент по указанному индексу из списка значений.
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806951"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="9bb00-103">Последовательно выберите пункты функции (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="9bb00-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="9bb00-104">Возвращает элемент по указанному индексу из списка значений.</span><span class="sxs-lookup"><span data-stu-id="9bb00-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9bb00-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9bb00-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="9bb00-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="9bb00-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9bb00-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bb00-107">Syntax</span></span>

<span data-ttu-id="9bb00-108">**Выбор** (*Номер_индекса*, *значение*[*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="9bb00-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="9bb00-109">Функция **Choose** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="9bb00-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="9bb00-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="9bb00-110">**Argument name**</span></span>|<span data-ttu-id="9bb00-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9bb00-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9bb00-112">*Номер_индекса*</span><span class="sxs-lookup"><span data-stu-id="9bb00-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="9bb00-113">Выражение целое число, представляющее индекс 1 в списке элементы его.</span><span class="sxs-lookup"><span data-stu-id="9bb00-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="9bb00-114">*Значение*</span><span class="sxs-lookup"><span data-stu-id="9bb00-114">*Value*</span></span>  <br/> |<span data-ttu-id="9bb00-115">Список значений любого типа данных.</span><span class="sxs-lookup"><span data-stu-id="9bb00-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bb00-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="9bb00-116">Remarks</span></span>

<span data-ttu-id="9bb00-117">Если предоставленный *номер_индекса* не является целым числом, значение неявно преобразуется в тип integer.</span><span class="sxs-lookup"><span data-stu-id="9bb00-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="9bb00-118">Если значение индекса превышает границ массива значений, **Choose** возвращает значение NULL.</span><span class="sxs-lookup"><span data-stu-id="9bb00-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

