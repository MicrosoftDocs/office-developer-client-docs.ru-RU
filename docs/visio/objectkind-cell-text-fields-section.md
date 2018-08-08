---
title: Ячейка ObjectKind (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Указывает тип текстового поля.
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814306"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="a9675-103">Ячейка ObjectKind (раздел "Текстовые поля")</span><span class="sxs-lookup"><span data-stu-id="a9675-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="a9675-104">Указывает тип текстового поля.</span><span class="sxs-lookup"><span data-stu-id="a9675-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="a9675-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a9675-105">**Value**</span></span>|<span data-ttu-id="a9675-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a9675-106">**Description**</span></span>|<span data-ttu-id="a9675-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="a9675-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a9675-108">0</span><span class="sxs-lookup"><span data-stu-id="a9675-108">0</span></span>  <br/> | <span data-ttu-id="a9675-109">Standard</span><span class="sxs-lookup"><span data-stu-id="a9675-109">Standard</span></span>  <br/> |<span data-ttu-id="a9675-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="a9675-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="a9675-111">1</span><span class="sxs-lookup"><span data-stu-id="a9675-111">1</span></span>  <br/> |<span data-ttu-id="a9675-112">Горизонтальный в вертикальном</span><span class="sxs-lookup"><span data-stu-id="a9675-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="a9675-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="a9675-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9675-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a9675-114">Remarks</span></span>

<span data-ttu-id="a9675-115">Текстовые поля может иметь одно из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="a9675-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="a9675-116">Стандарт, указывающего на то, что поле был вставлен по категориям поля.</span><span class="sxs-lookup"><span data-stu-id="a9675-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="a9675-117">Горизонтальный в вертикальном, указывает, что поле горизонтальный в вертикальном текст.</span><span class="sxs-lookup"><span data-stu-id="a9675-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="a9675-118">Чтобы получить ссылку на ячейку ObjectKind по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a9675-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9675-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a9675-119">Cell name:</span></span>  <br/> | <span data-ttu-id="a9675-120">Fields.ObjectKind [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a9675-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a9675-121">Для получения ссылки на ячейки ObjectKind по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a9675-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9675-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a9675-122">Section index:</span></span>  <br/> |<span data-ttu-id="a9675-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="a9675-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="a9675-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a9675-124">Row index:</span></span>  <br/> |<span data-ttu-id="a9675-125">**visRowField** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a9675-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a9675-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a9675-126">Cell index:</span></span>  <br/> |<span data-ttu-id="a9675-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="a9675-127">**visFieldObjectKind**</span></span> <br/> |
   

