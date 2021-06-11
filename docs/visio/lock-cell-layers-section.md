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
description: Указывает, заблокированы ли фигуры, принадлежащие к слою, от выбора или редактирования.
ms.openlocfilehash: d548a6f0fe0cac10d80d73c904739b2979ecf27f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438829"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="47a07-103">Lock Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="47a07-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="47a07-104">Указывает, заблокированы ли фигуры, принадлежащие к слою, от выбора или редактирования.</span><span class="sxs-lookup"><span data-stu-id="47a07-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="47a07-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="47a07-105">**Value**</span></span>|<span data-ttu-id="47a07-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="47a07-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47a07-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="47a07-107">TRUE</span></span>  <br/> |<span data-ttu-id="47a07-108">Фигуры заблокированы.</span><span class="sxs-lookup"><span data-stu-id="47a07-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="47a07-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="47a07-109">FALSE</span></span>  <br/> |<span data-ttu-id="47a07-110">Фигуры не заблокированы.</span><span class="sxs-lookup"><span data-stu-id="47a07-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47a07-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="47a07-111">Remarks</span></span>

<span data-ttu-id="47a07-112">Вы также можете установить это  значение, выбрав блокировку в диалоговом окне **Свойства** слоя (на вкладке **Home,** в группе редактирования щелкните Слои **и** нажмите кнопку **Свойства слоя).** </span><span class="sxs-lookup"><span data-stu-id="47a07-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="47a07-113">Чтобы получить ссылку на ячейку Блокировка по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="47a07-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47a07-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="47a07-114">Cell name:</span></span>  <br/> |<span data-ttu-id="47a07-115">Layers.Locked[i] где *i* = <1>, 2, 3... </span><span class="sxs-lookup"><span data-stu-id="47a07-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="47a07-116">Чтобы получить ссылку на ячейку Блокировка по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="47a07-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47a07-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="47a07-117">Section index:</span></span>  <br/> |<span data-ttu-id="47a07-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="47a07-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="47a07-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="47a07-119">Row index:</span></span>  <br/> |<span data-ttu-id="47a07-120">**visRowLayer**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="47a07-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="47a07-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="47a07-121">Cell index:</span></span>  <br/> |<span data-ttu-id="47a07-122">**visLayerLock**</span><span class="sxs-lookup"><span data-stu-id="47a07-122">**visLayerLock**</span></span> <br/> |
   

