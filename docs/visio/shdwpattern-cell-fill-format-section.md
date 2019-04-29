---
title: ShdwPattern Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Определяет узор заливки для тени фигуры.
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427614"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="77b62-103">ShdwPattern Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="77b62-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="77b62-104">Определяет узор заливки для тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="77b62-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="77b62-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="77b62-105">**Value**</span></span>|<span data-ttu-id="77b62-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77b62-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77b62-107">нуль</span><span class="sxs-lookup"><span data-stu-id="77b62-107">0</span></span>  <br/> |<span data-ttu-id="77b62-108">Нет (прозрачная заливка)</span><span class="sxs-lookup"><span data-stu-id="77b62-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="77b62-109">1,1</span><span class="sxs-lookup"><span data-stu-id="77b62-109">1</span></span>  <br/> |<span data-ttu-id="77b62-110">Сплошной цвет переднего плана</span><span class="sxs-lookup"><span data-stu-id="77b62-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="77b62-111">2-40</span><span class="sxs-lookup"><span data-stu-id="77b62-111">2 - 40</span></span>  <br/> |<span data-ttu-id="77b62-112">Шаблоны ассортимента</span><span class="sxs-lookup"><span data-stu-id="77b62-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77b62-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="77b62-113">Remarks</span></span>

<span data-ttu-id="77b62-114">Чтобы задать шаблон Fill, введите число от 0 до 40, которое представляет собой индекс в коллекции шаблонов.</span><span class="sxs-lookup"><span data-stu-id="77b62-114">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns.</span></span> <span data-ttu-id="77b62-115">Вы можете просмотреть коллекцию шаблонов заливки в диалоговом окне **Заливка** (на вкладке **Главная** , в группе **фигур** нажмите кнопку **Заливка**, а затем выберите команду **Параметры заливки**).</span><span class="sxs-lookup"><span data-stu-id="77b62-115">You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="77b62-116">Чтобы получить ссылку на ячейку ShdwPattern по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="77b62-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77b62-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="77b62-117">Cell name:</span></span>  <br/> |<span data-ttu-id="77b62-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="77b62-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="77b62-119">Чтобы получить ссылку на ячейку ShdwPattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="77b62-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77b62-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="77b62-120">Section index:</span></span>  <br/> |<span data-ttu-id="77b62-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="77b62-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="77b62-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="77b62-122">Row index:</span></span>  <br/> |<span data-ttu-id="77b62-123">**Висровфилл**</span><span class="sxs-lookup"><span data-stu-id="77b62-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="77b62-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="77b62-124">Cell index:</span></span>  <br/> |<span data-ttu-id="77b62-125">**Висфиллшдвпаттерн**</span><span class="sxs-lookup"><span data-stu-id="77b62-125">**visFillShdwPattern**</span></span> <br/> |
   

