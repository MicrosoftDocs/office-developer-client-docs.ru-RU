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
description: Указывает, вставлен ли в меню над этим действием сепаратор.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407839"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="3801e-103">BeginGroup Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="3801e-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="3801e-104">Указывает, вставлен ли в меню над этим действием сепаратор.</span><span class="sxs-lookup"><span data-stu-id="3801e-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="3801e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3801e-105">**Value**</span></span>|<span data-ttu-id="3801e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3801e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3801e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3801e-107">TRUE</span></span>  <br/> |<span data-ttu-id="3801e-108">В меню над этим действием вставляется сепаратор.</span><span class="sxs-lookup"><span data-stu-id="3801e-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="3801e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3801e-109">FALSE</span></span>  <br/> |<span data-ttu-id="3801e-110">В меню над этим действием (по умолчанию) не вставляется сепаратор.</span><span class="sxs-lookup"><span data-stu-id="3801e-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3801e-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="3801e-111">Remarks</span></span>

<span data-ttu-id="3801e-112">Чтобы получить ссылку на ячейку BeginGroup по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="3801e-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3801e-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3801e-113">Cell name:</span></span>  <br/> |<span data-ttu-id="3801e-114">Действия.</span><span class="sxs-lookup"><span data-stu-id="3801e-114">Actions.</span></span> <span data-ttu-id="3801e-115">*имя*. BeginGroup, где действия.</span><span class="sxs-lookup"><span data-stu-id="3801e-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="3801e-116">*имя* — это имя строки Действия</span><span class="sxs-lookup"><span data-stu-id="3801e-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="3801e-117">Чтобы получить ссылку на ячейку BeginGroup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3801e-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3801e-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3801e-118">Section index:</span></span>  <br/> |<span data-ttu-id="3801e-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="3801e-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="3801e-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3801e-120">Row index:</span></span>  <br/> |<span data-ttu-id="3801e-121">**visRowAction**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="3801e-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3801e-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3801e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3801e-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="3801e-123">**visActionBeginGroup**</span></span> <br/> |
   

