---
title: Ячейка TextDirection (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Определяет направление символов в блоке текста.
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815021"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="32834-103">Ячейка TextDirection (раздел "Формат текстового блока")</span><span class="sxs-lookup"><span data-stu-id="32834-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="32834-104">Определяет направление символов в блоке текста.</span><span class="sxs-lookup"><span data-stu-id="32834-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="32834-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="32834-105">**Value**</span></span>|<span data-ttu-id="32834-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="32834-106">**Direction**</span></span>|<span data-ttu-id="32834-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="32834-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="32834-108">0</span><span class="sxs-lookup"><span data-stu-id="32834-108">0</span></span>  <br/> | <span data-ttu-id="32834-109">Горизонтальная</span><span class="sxs-lookup"><span data-stu-id="32834-109">Horizontal</span></span>  <br/> |<span data-ttu-id="32834-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="32834-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="32834-111">1</span><span class="sxs-lookup"><span data-stu-id="32834-111">1</span></span>  <br/> | <span data-ttu-id="32834-112">По вертикали</span><span class="sxs-lookup"><span data-stu-id="32834-112">Vertical</span></span>  <br/> |<span data-ttu-id="32834-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="32834-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32834-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="32834-114">Remarks</span></span>

<span data-ttu-id="32834-115">В продуктах японского языка версии 5.0 Visio значение ячейки была сохранена в ячейке VerticalText в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="32834-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="32834-116">Чтобы получить ссылку на ячейку TextDirection по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="32834-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32834-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="32834-117">Cell name:</span></span>  <br/> | <span data-ttu-id="32834-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="32834-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="32834-119">Для получения ссылки на ячейки TextDirection по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="32834-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32834-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="32834-120">Section index:</span></span>  <br/> |<span data-ttu-id="32834-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="32834-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="32834-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="32834-122">Row index:</span></span>  <br/> |<span data-ttu-id="32834-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="32834-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="32834-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="32834-124">Cell index:</span></span>  <br/> |<span data-ttu-id="32834-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="32834-125">**visTxtBlkDirection**</span></span> <br/> |
   

