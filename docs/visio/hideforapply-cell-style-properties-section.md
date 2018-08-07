---
title: Ячейка HideForApply (раздел "Свойства стиля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Определяет, где стиля отображается в интерфейсе пользователя Microsoft Visio.
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813918"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="26c25-103">Ячейка HideForApply (раздел "Свойства стиля")</span><span class="sxs-lookup"><span data-stu-id="26c25-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="26c25-104">Определяет, где стиля отображается в интерфейсе пользователя Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="26c25-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="26c25-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="26c25-105">**Value**</span></span>|<span data-ttu-id="26c25-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="26c25-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="26c25-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="26c25-107">TRUE</span></span>  <br/> | <span data-ttu-id="26c25-108">Показать стиль только в **Обозревателе документа**.</span><span class="sxs-lookup"><span data-stu-id="26c25-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="26c25-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="26c25-109">FALSE</span></span>  <br/> | <span data-ttu-id="26c25-110">Показать стиль в **Обозревателе документа**.</span><span class="sxs-lookup"><span data-stu-id="26c25-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26c25-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="26c25-111">Remarks</span></span>

<span data-ttu-id="26c25-112">Если новый стиль основывается на стиль, который скрыт, новый стиль не наследует этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="26c25-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="26c25-113">Чтобы получить ссылку на ячейку HideForApply по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="26c25-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="26c25-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="26c25-114">Cell name:</span></span>  <br/> | <span data-ttu-id="26c25-115">HideForApply</span><span class="sxs-lookup"><span data-stu-id="26c25-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="26c25-116">Для получения ссылки на ячейки HideForApply по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="26c25-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="26c25-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="26c25-117">Section index:</span></span>  <br/> |<span data-ttu-id="26c25-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="26c25-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="26c25-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="26c25-119">Row index:</span></span>  <br/> |<span data-ttu-id="26c25-120">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="26c25-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="26c25-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="26c25-121">Cell index:</span></span>  <br/> |<span data-ttu-id="26c25-122">**visStyleHidden**</span><span class="sxs-lookup"><span data-stu-id="26c25-122">**visStyleHidden**</span></span> <br/> |
   

