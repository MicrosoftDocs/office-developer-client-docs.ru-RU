---
title: Ячейка Description (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Представляет строку описательный текст гиперссылки.
ms.openlocfilehash: 567a90b3162c109582c3149c156a994392980577
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813613"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="70409-103">Ячейка Description (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="70409-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="70409-104">Представляет строку описательный текст гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="70409-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="70409-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="70409-105">Remarks</span></span>

<span data-ttu-id="70409-106">Используйте эту ячейку для хранения комментариев о гиперссылках; Например «ссылка на наш цен веб-сайта».</span><span class="sxs-lookup"><span data-stu-id="70409-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing Web site."</span></span>
  
<span data-ttu-id="70409-107">Можно также задать значение данной ячейки в диалоговом окне **гиперссылки** (щелкните **гиперссылку** на вкладке **Вставка** ).</span><span class="sxs-lookup"><span data-stu-id="70409-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="70409-108">Для получения ссылки на ячейки описание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="70409-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70409-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="70409-109">Cell name:</span></span>  <br/> | <span data-ttu-id="70409-110">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="70409-110">Hyperlink.</span></span>  <span data-ttu-id="70409-111">*Имя* . Описание где гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="70409-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="70409-112">*Имя* — это имя строки гиперссылки</span><span class="sxs-lookup"><span data-stu-id="70409-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="70409-113">Для получения ссылки на ячейки описание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="70409-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70409-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="70409-114">Section index:</span></span>  <br/> |<span data-ttu-id="70409-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="70409-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="70409-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="70409-116">Row index:</span></span>  <br/> |<span data-ttu-id="70409-117">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="70409-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="70409-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="70409-118">Cell index:</span></span>  <br/> |<span data-ttu-id="70409-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="70409-119">**visHLinkDescription**</span></span> <br/> |
   

