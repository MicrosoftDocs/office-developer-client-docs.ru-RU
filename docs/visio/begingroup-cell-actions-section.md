---
title: BeginGroup Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Указывает, вставляется ли разделитель в меню над этим действием.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407839"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="fe815-103">BeginGroup Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="fe815-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="fe815-104">Указывает, вставляется ли разделитель в меню над этим действием.</span><span class="sxs-lookup"><span data-stu-id="fe815-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="fe815-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fe815-105">**Value**</span></span>|<span data-ttu-id="fe815-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe815-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe815-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fe815-107">TRUE</span></span>  <br/> |<span data-ttu-id="fe815-108">В меню над этим действием вставляется разделитель.</span><span class="sxs-lookup"><span data-stu-id="fe815-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="fe815-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fe815-109">FALSE</span></span>  <br/> |<span data-ttu-id="fe815-110">Разделитель не вставляется в меню над этим действием (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="fe815-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe815-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe815-111">Remarks</span></span>

<span data-ttu-id="fe815-112">Чтобы получить ссылку на ячейку BeginGroup по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="fe815-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe815-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fe815-113">Cell name:</span></span>  <br/> |<span data-ttu-id="fe815-114">Действия.</span><span class="sxs-lookup"><span data-stu-id="fe815-114">Actions.</span></span> <span data-ttu-id="fe815-115">*Name (имя*). BeginGroup, где Actions.</span><span class="sxs-lookup"><span data-stu-id="fe815-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="fe815-116">*Name* — имя строки действий</span><span class="sxs-lookup"><span data-stu-id="fe815-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="fe815-117">Чтобы получить ссылку на ячейку BeginGroup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fe815-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe815-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fe815-118">Section index:</span></span>  <br/> |<span data-ttu-id="fe815-119">**виссектионактион**</span><span class="sxs-lookup"><span data-stu-id="fe815-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="fe815-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fe815-120">Row index:</span></span>  <br/> |<span data-ttu-id="fe815-121">**висровактион** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fe815-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="fe815-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fe815-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fe815-123">**висактионбегинграуп**</span><span class="sxs-lookup"><span data-stu-id="fe815-123">**visActionBeginGroup**</span></span> <br/> |
   

