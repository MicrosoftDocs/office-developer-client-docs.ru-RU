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
description: Представляет текстовую строку для гиперссылки.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360244"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="4f0c8-103">Description Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="4f0c8-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="4f0c8-104">Представляет текстовую строку для гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="4f0c8-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4f0c8-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f0c8-105">Remarks</span></span>

<span data-ttu-id="4f0c8-106">Используйте эту ячейку для хранения комментариев о гиперссылке; например, "Ссылка на наш веб-сайт цен".</span><span class="sxs-lookup"><span data-stu-id="4f0c8-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="4f0c8-107">Вы также можете установить значение этой  ячейки в диалоговом окне "Гиперссылки" (щелкните **"Гиперссылка"** на вкладке **"Вставка").**</span><span class="sxs-lookup"><span data-stu-id="4f0c8-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="4f0c8-108">Чтобы получить ссылку на ячейку Description по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4f0c8-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f0c8-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4f0c8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="4f0c8-110">Гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="4f0c8-110">Hyperlink.</span></span>  <span data-ttu-id="4f0c8-111">*Name*  . Описание гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="4f0c8-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="4f0c8-112">*Имя*  — имя строки гиперссылки</span><span class="sxs-lookup"><span data-stu-id="4f0c8-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="4f0c8-113">Чтобы получить ссылку на ячейку Description по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4f0c8-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f0c8-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4f0c8-114">Section index:</span></span>  <br/> |<span data-ttu-id="4f0c8-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="4f0c8-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="4f0c8-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4f0c8-116">Row index:</span></span>  <br/> |<span data-ttu-id="4f0c8-117">**visRow1stHyperlink**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4f0c8-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4f0c8-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4f0c8-118">Cell index:</span></span>  <br/> |<span data-ttu-id="4f0c8-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="4f0c8-119">**visHLinkDescription**</span></span> <br/> |
   

