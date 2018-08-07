---
title: Ячейка ShdwPattern (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Определяет узор заливки для тени фигуры.
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814832"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="492f9-103">Ячейка ShdwPattern (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="492f9-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="492f9-104">Определяет узор заливки для тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="492f9-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="492f9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="492f9-105">**Value**</span></span>|<span data-ttu-id="492f9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="492f9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="492f9-107">0</span><span class="sxs-lookup"><span data-stu-id="492f9-107">0</span></span>  <br/> |<span data-ttu-id="492f9-108">None (прозрачной заливки)</span><span class="sxs-lookup"><span data-stu-id="492f9-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="492f9-109">1</span><span class="sxs-lookup"><span data-stu-id="492f9-109">1</span></span>  <br/> |<span data-ttu-id="492f9-110">Сплошной цвет</span><span class="sxs-lookup"><span data-stu-id="492f9-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="492f9-111">2 - 40</span><span class="sxs-lookup"><span data-stu-id="492f9-111">2 - 40</span></span>  <br/> |<span data-ttu-id="492f9-112">В этой модели</span><span class="sxs-lookup"><span data-stu-id="492f9-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="492f9-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="492f9-113">Remarks</span></span>

<span data-ttu-id="492f9-114">Чтобы задать шаблон заполнения, введите число от 0 до 40, которая является индексом в коллекции шаблонов.</span><span class="sxs-lookup"><span data-stu-id="492f9-114">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns.</span></span> <span data-ttu-id="492f9-115">Шаблон заполнения коллекции можно просмотреть в диалоговом окне **заливки** (на вкладке **Главная** в группе **фигуры** щелкните **заливки**и выберите пункт **Параметры заливки**).</span><span class="sxs-lookup"><span data-stu-id="492f9-115">You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="492f9-116">Чтобы получить ссылку на ячейку ShdwPattern по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="492f9-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="492f9-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="492f9-117">Cell name:</span></span>  <br/> |<span data-ttu-id="492f9-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="492f9-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="492f9-119">Для получения ссылки на ячейки ShdwPattern по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="492f9-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="492f9-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="492f9-120">Section index:</span></span>  <br/> |<span data-ttu-id="492f9-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="492f9-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="492f9-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="492f9-122">Row index:</span></span>  <br/> |<span data-ttu-id="492f9-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="492f9-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="492f9-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="492f9-124">Cell index:</span></span>  <br/> |<span data-ttu-id="492f9-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="492f9-125">**visFillShdwPattern**</span></span> <br/> |
   

