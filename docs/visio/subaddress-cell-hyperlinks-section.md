---
title: Ячейка SubAddress (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Указывает расположение в документе, чтобы связать.
ms.openlocfilehash: 0509b9b6a708924b5aeb69f16f3f4cd99573cc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814972"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="099cd-103">Ячейка SubAddress (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="099cd-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="099cd-104">Указывает расположение в документе, чтобы связать.</span><span class="sxs-lookup"><span data-stu-id="099cd-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="099cd-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="099cd-105">Remarks</span></span>

<span data-ttu-id="099cd-106">К примеру Если ячейка адрес «Drawing1.vsdx», дополнительный адрес ячейки можно указать имя страницы, например «страница 3".</span><span class="sxs-lookup"><span data-stu-id="099cd-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="099cd-107">Если адрес ячейка находится файл Microsoft Excel «Samples.xlsx», значение ячейки может быть листа или диапазона, листа, например, «Функции» или «Sheet1! A1:D10».</span><span class="sxs-lookup"><span data-stu-id="099cd-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="099cd-108">Если ячейка адрес "http://www.microsoft.com/office/«, значение ячейки может быть имя привязки в документе, такими как «решения».</span><span class="sxs-lookup"><span data-stu-id="099cd-108">If the Address cell is "http://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="099cd-109">Можно также задать значение данной ячейки в диалоговом окне " **гиперссылки** " (в группе **ссылки** на вкладке **Вставка** выберите **гиперссылку**).</span><span class="sxs-lookup"><span data-stu-id="099cd-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="099cd-110">Чтобы получить ссылку на ячейку дополнительный адрес по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="099cd-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="099cd-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="099cd-111">Cell name:</span></span>  <br/> | <span data-ttu-id="099cd-112">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="099cd-112">Hyperlink.</span></span>  <span data-ttu-id="099cd-113">*имя* . Дополнительный адрес, где гиперссылки *.name* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="099cd-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="099cd-114">Для получения ссылки на ячейки **дополнительный адрес** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="099cd-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="099cd-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="099cd-115">Section index:</span></span>  <br/> |<span data-ttu-id="099cd-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="099cd-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="099cd-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="099cd-117">Row index:</span></span>  <br/> |<span data-ttu-id="099cd-118">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="099cd-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="099cd-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="099cd-119">Cell index:</span></span>  <br/> |<span data-ttu-id="099cd-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="099cd-120">**visHLinkSubAddress**</span></span> <br/> |
   

