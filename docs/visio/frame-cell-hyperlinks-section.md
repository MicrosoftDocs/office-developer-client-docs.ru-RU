---
title: Frame Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Представляет имя целевого кадра, когда приложение открыто в качестве активного документа в приложении-контейнере. Значение по умолчанию — пустая строка.
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432858"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="208b6-104">Frame Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="208b6-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="208b6-105">Представляет имя целевого кадра, когда приложение открыто в качестве активного документа в приложении-контейнере.</span><span class="sxs-lookup"><span data-stu-id="208b6-105">Represents the name of a frame to target when the application is open as an Active document in a container application.</span></span> <span data-ttu-id="208b6-106">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="208b6-106">The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="208b6-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="208b6-107">Remarks</span></span>

<span data-ttu-id="208b6-108">Чтобы получить ссылку на ячейку Frame по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="208b6-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="208b6-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="208b6-109">Cell name:</span></span>  <br/> | <span data-ttu-id="208b6-110">Гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="208b6-110">Hyperlink.</span></span>  <span data-ttu-id="208b6-111">*name*  . Кадр, в котором находится гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="208b6-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="208b6-112">*name*  — имя строки</span><span class="sxs-lookup"><span data-stu-id="208b6-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="208b6-113">Чтобы получить ссылку на ячейку Frame по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="208b6-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="208b6-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="208b6-114">Section index:</span></span>  <br/> |<span data-ttu-id="208b6-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="208b6-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="208b6-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="208b6-116">Row index:</span></span>  <br/> |<span data-ttu-id="208b6-117">**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="208b6-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="208b6-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="208b6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="208b6-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="208b6-119">**visHLinkFrame**</span></span> <br/> |
   

