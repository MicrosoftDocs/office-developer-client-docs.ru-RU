---
title: ObjectKind Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Указывает тип текстового поля.
ms.openlocfilehash: c2f891620f704a3c48861124b886e49d356960ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438514"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="fa8bc-103">ObjectKind Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="fa8bc-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="fa8bc-104">Указывает тип текстового поля.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="fa8bc-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fa8bc-105">**Value**</span></span>|<span data-ttu-id="fa8bc-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fa8bc-106">**Description**</span></span>|<span data-ttu-id="fa8bc-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="fa8bc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="fa8bc-108">0</span><span class="sxs-lookup"><span data-stu-id="fa8bc-108">0</span></span>  <br/> | <span data-ttu-id="fa8bc-109">Стандартный</span><span class="sxs-lookup"><span data-stu-id="fa8bc-109">Standard</span></span>  <br/> |<span data-ttu-id="fa8bc-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="fa8bc-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="fa8bc-111">1 </span><span class="sxs-lookup"><span data-stu-id="fa8bc-111">1</span></span>  <br/> |<span data-ttu-id="fa8bc-112">Горизонтальный по вертикали</span><span class="sxs-lookup"><span data-stu-id="fa8bc-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="fa8bc-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="fa8bc-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa8bc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa8bc-114">Remarks</span></span>

<span data-ttu-id="fa8bc-115">Текстовые поля могут иметь один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="fa8bc-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="fa8bc-116">Стандартная, указывающая, что поле было вставлено по категории полей.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="fa8bc-117">По горизонтали по вертикали, указывая, что поле является горизонтальным текстом, установленным в вертикальном тексте.</span><span class="sxs-lookup"><span data-stu-id="fa8bc-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="fa8bc-118">Чтобы получить ссылку на ячейку ObjectKind по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fa8bc-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa8bc-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fa8bc-119">Cell name:</span></span>  <br/> | <span data-ttu-id="fa8bc-120">Fields.ObjectKind[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fa8bc-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fa8bc-121">Чтобы получить ссылку на ячейку ObjectKind по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fa8bc-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa8bc-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fa8bc-122">Section index:</span></span>  <br/> |<span data-ttu-id="fa8bc-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="fa8bc-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="fa8bc-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fa8bc-124">Row index:</span></span>  <br/> |<span data-ttu-id="fa8bc-125">**visRowField**  +   *i,* *где i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fa8bc-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fa8bc-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fa8bc-126">Cell index:</span></span>  <br/> |<span data-ttu-id="fa8bc-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="fa8bc-127">**visFieldObjectKind**</span></span> <br/> |
   

