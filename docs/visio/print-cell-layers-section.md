---
title: Ячейка Print (раздел "Слои")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Указывает, можно ли печатать фигур, относящегося к слою.
ms.openlocfilehash: cd5b2830ba8bd20cb435cdc2bca4bd55fd5a5438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814483"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="bdc41-103">Ячейка Print (раздел "Слои")</span><span class="sxs-lookup"><span data-stu-id="bdc41-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="bdc41-104">Указывает, можно ли печатать фигур, относящегося к слою.</span><span class="sxs-lookup"><span data-stu-id="bdc41-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="bdc41-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="bdc41-105">**Value**</span></span>|<span data-ttu-id="bdc41-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bdc41-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bdc41-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bdc41-107">TRUE</span></span>  <br/> |<span data-ttu-id="bdc41-108">Можно распечатать фигур.</span><span class="sxs-lookup"><span data-stu-id="bdc41-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="bdc41-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bdc41-109">FALSE</span></span>  <br/> |<span data-ttu-id="bdc41-110">Не удается напечатать фигур.</span><span class="sxs-lookup"><span data-stu-id="bdc41-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdc41-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="bdc41-111">Remarks</span></span>

<span data-ttu-id="bdc41-112">Также можно задать это значение с помощью параметра **печати** в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer**).</span><span class="sxs-lookup"><span data-stu-id="bdc41-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="bdc41-113">Для получения ссылки на ячейки Print по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bdc41-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bdc41-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="bdc41-114">Cell name:</span></span>  <br/> |<span data-ttu-id="bdc41-115">Layers.Print [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bdc41-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bdc41-116">Для получения ссылки на ячейки Print по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="bdc41-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bdc41-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bdc41-117">Section index:</span></span>  <br/> |<span data-ttu-id="bdc41-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="bdc41-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="bdc41-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bdc41-119">Row index:</span></span>  <br/> |<span data-ttu-id="bdc41-120">**visRowLayer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bdc41-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="bdc41-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bdc41-121">Cell index:</span></span>  <br/> |<span data-ttu-id="bdc41-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="bdc41-122">**visDocPreviewScope**</span></span> <br/> |
   

