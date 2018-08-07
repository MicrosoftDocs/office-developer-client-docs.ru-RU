---
title: Ячейка FillPattern (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Определяет узор заливки для фигуры. Чтобы указать пользовательский узор заливки, используйте функцию использования в этой ячейке.
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813765"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="3926c-104">Ячейка FillPattern (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="3926c-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="3926c-105">Определяет узор заливки для фигуры.</span><span class="sxs-lookup"><span data-stu-id="3926c-105">Determines the fill pattern for the shape.</span></span> <span data-ttu-id="3926c-106">Чтобы указать пользовательский узор заливки, используйте функцию использования в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="3926c-106">To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="3926c-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3926c-107">**Value**</span></span>|<span data-ttu-id="3926c-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3926c-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3926c-109">0</span><span class="sxs-lookup"><span data-stu-id="3926c-109">0</span></span>  <br/> |<span data-ttu-id="3926c-110">None (прозрачной заливки).</span><span class="sxs-lookup"><span data-stu-id="3926c-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="3926c-111">1</span><span class="sxs-lookup"><span data-stu-id="3926c-111">1</span></span>  <br/> |<span data-ttu-id="3926c-112">Сплошной цвет.</span><span class="sxs-lookup"><span data-stu-id="3926c-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="3926c-113">2 - 40</span><span class="sxs-lookup"><span data-stu-id="3926c-113">2 - 40</span></span>  <br/> |<span data-ttu-id="3926c-114">Шаблоны различные заполнения, соответствующие индексирование записей в диалоговом окне **заливки** .</span><span class="sxs-lookup"><span data-stu-id="3926c-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3926c-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="3926c-115">Remarks</span></span>

<span data-ttu-id="3926c-116">Также можно задать это значение, с помощью диалогового окна **заполните поля** (на вкладке **Главная** в группе **фигуры** выберите **заполните поля** и нажмите кнопку **Параметры заливки**).</span><span class="sxs-lookup"><span data-stu-id="3926c-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="3926c-117">Чтобы получить ссылку на ячейку узор заливки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3926c-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3926c-118">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="3926c-118">Cell name:</span></span>  <br/> |<span data-ttu-id="3926c-119">Узор заливки</span><span class="sxs-lookup"><span data-stu-id="3926c-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="3926c-120">Для получения ссылки на ячейки узор заливки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="3926c-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3926c-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3926c-121">Section index:</span></span>  <br/> |<span data-ttu-id="3926c-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3926c-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3926c-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3926c-123">Row index:</span></span>  <br/> |<span data-ttu-id="3926c-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="3926c-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="3926c-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3926c-125">Cell index:</span></span>  <br/> |<span data-ttu-id="3926c-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="3926c-126">**visFillPattern**</span></span> <br/> |
   

