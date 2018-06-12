---
title: Ячейка TxtPinY (раздел Преобразование текст)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Определяет, y-координата блок текста центра вращения относительно начала фигуры. Формула по умолчанию имеет вид:'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815084"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="cbe65-104">Ячейка TxtPinY (раздел Преобразование текст)</span><span class="sxs-lookup"><span data-stu-id="cbe65-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="cbe65-105">Определяет, *y* -координата блок текста центра вращения относительно начала фигуры.</span><span class="sxs-lookup"><span data-stu-id="cbe65-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="cbe65-106">Формула по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="cbe65-106">The default formula is:</span></span> 
  
<span data-ttu-id="cbe65-107">= Высота \* 0,5</span><span class="sxs-lookup"><span data-stu-id="cbe65-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cbe65-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="cbe65-108">Remarks</span></span>

<span data-ttu-id="cbe65-109">Чтобы получить ссылку на ячейку TxtPinY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cbe65-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cbe65-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="cbe65-110">Cell name:</span></span>  <br/> | <span data-ttu-id="cbe65-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="cbe65-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="cbe65-112">Для получения ссылки на ячейки TxtPinY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="cbe65-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cbe65-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cbe65-113">Section index:</span></span>  <br/> |<span data-ttu-id="cbe65-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cbe65-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cbe65-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cbe65-115">Row index:</span></span>  <br/> |<span data-ttu-id="cbe65-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="cbe65-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="cbe65-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cbe65-117">Cell index:</span></span>  <br/> |<span data-ttu-id="cbe65-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="cbe65-118">**visXFormPinY**</span></span> <br/> |
   

