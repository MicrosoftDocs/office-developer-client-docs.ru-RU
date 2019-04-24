---
title: Lock Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Указывает, заблокированы ли фигуры, принадлежащие слою, для выбора или изменения.
ms.openlocfilehash: d548a6f0fe0cac10d80d73c904739b2979ecf27f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359684"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="3973f-103">Lock Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="3973f-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="3973f-104">Указывает, заблокированы ли фигуры, принадлежащие слою, для выбора или изменения.</span><span class="sxs-lookup"><span data-stu-id="3973f-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="3973f-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="3973f-105">**Value**</span></span>|<span data-ttu-id="3973f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3973f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3973f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3973f-107">TRUE</span></span>  <br/> |<span data-ttu-id="3973f-108">Фигуры заблокированы.</span><span class="sxs-lookup"><span data-stu-id="3973f-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="3973f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3973f-109">FALSE</span></span>  <br/> |<span data-ttu-id="3973f-110">Фигуры не блокируются.</span><span class="sxs-lookup"><span data-stu-id="3973f-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3973f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="3973f-111">Remarks</span></span>

<span data-ttu-id="3973f-112">Вы также можете задать это значение, выбрав пункт **Блокировка** в диалоговом окне **Свойства слоя** (на вкладке **Главная** , в группе **Правка** щелкните **слои**, а затем выберите **Свойства слоя**).</span><span class="sxs-lookup"><span data-stu-id="3973f-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="3973f-113">Чтобы получить ссылку на ячейку Lock по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="3973f-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3973f-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3973f-114">Cell name:</span></span>  <br/> |<span data-ttu-id="3973f-115">Слои. заблокировано [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3973f-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3973f-116">Чтобы получить ссылку на ячейку Lock по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3973f-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3973f-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3973f-117">Section index:</span></span>  <br/> |<span data-ttu-id="3973f-118">**Виссектионлайер**</span><span class="sxs-lookup"><span data-stu-id="3973f-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="3973f-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3973f-119">Row index:</span></span>  <br/> |<span data-ttu-id="3973f-120">**висровлайер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3973f-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3973f-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3973f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="3973f-122">**Вислайерлокк**</span><span class="sxs-lookup"><span data-stu-id="3973f-122">**visLayerLock**</span></span> <br/> |
   

