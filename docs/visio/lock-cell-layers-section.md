---
title: Блокирование ячейки (слои раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Указывает, заблокирован ли фигур, относящегося к слою от выбора и редактирования.
ms.openlocfilehash: f404fe15814de802f4f6bfcebfd2558cf10cc7eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814112"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="8e14f-103">Блокирование ячейки (слои раздел)</span><span class="sxs-lookup"><span data-stu-id="8e14f-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="8e14f-104">Указывает, заблокирован ли фигур, относящегося к слою от выбора и редактирования.</span><span class="sxs-lookup"><span data-stu-id="8e14f-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="8e14f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8e14f-105">**Value**</span></span>|<span data-ttu-id="8e14f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e14f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e14f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8e14f-107">TRUE</span></span>  <br/> |<span data-ttu-id="8e14f-108">Фигуры заблокированы.</span><span class="sxs-lookup"><span data-stu-id="8e14f-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="8e14f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8e14f-109">FALSE</span></span>  <br/> |<span data-ttu-id="8e14f-110">Фигуры не блокируется.</span><span class="sxs-lookup"><span data-stu-id="8e14f-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e14f-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="8e14f-111">Remarks</span></span>

<span data-ttu-id="8e14f-112">Также можно задать это значение, выбрав **блокировки** в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer**).</span><span class="sxs-lookup"><span data-stu-id="8e14f-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="8e14f-113">Для получения ссылки на ячейки блокировки по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8e14f-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e14f-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8e14f-114">Cell name:</span></span>  <br/> |<span data-ttu-id="8e14f-115">Layers.Locked [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8e14f-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8e14f-116">Для получения ссылки на ячейки блокировки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8e14f-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e14f-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8e14f-117">Section index:</span></span>  <br/> |<span data-ttu-id="8e14f-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="8e14f-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="8e14f-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8e14f-119">Row index:</span></span>  <br/> |<span data-ttu-id="8e14f-120">**visRowLayer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8e14f-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="8e14f-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8e14f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="8e14f-122">**visLayerLock**</span><span class="sxs-lookup"><span data-stu-id="8e14f-122">**visLayerLock**</span></span> <br/> |
   

