---
title: Description Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Представляет строку с описанием для гиперссылки.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360244"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="a6df9-103">Description Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="a6df9-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="a6df9-104">Представляет строку с описанием для гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="a6df9-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6df9-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6df9-105">Remarks</span></span>

<span data-ttu-id="a6df9-106">Используйте эту ячейку для хранения комментариев относительно гиперссылки; Пример: "ссылка на наш веб-сайт ценообразования".</span><span class="sxs-lookup"><span data-stu-id="a6df9-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="a6df9-107">Значение этой ячейки также можно задать в диалоговом окне **гиперссылки** (щелкните **Гиперссылка** на вкладке **Вставка** ).</span><span class="sxs-lookup"><span data-stu-id="a6df9-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="a6df9-108">Чтобы получить ссылку на ячейку Description по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="a6df9-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6df9-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a6df9-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a6df9-110">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="a6df9-110">Hyperlink.</span></span>  <span data-ttu-id="a6df9-111">*Name (имя* ). Description, где Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="a6df9-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="a6df9-112">*Name* — имя строки гиперссылки</span><span class="sxs-lookup"><span data-stu-id="a6df9-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="a6df9-113">Чтобы получить ссылку на ячейку Description по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a6df9-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6df9-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a6df9-114">Section index:</span></span>  <br/> |<span data-ttu-id="a6df9-115">**виссектионхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="a6df9-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="a6df9-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a6df9-116">Row index:</span></span>  <br/> |<span data-ttu-id="a6df9-117">**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a6df9-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a6df9-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a6df9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a6df9-119">**вишлинкдескриптион**</span><span class="sxs-lookup"><span data-stu-id="a6df9-119">**visHLinkDescription**</span></span> <br/> |
   

