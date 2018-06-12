---
title: Без проверки ячейки (раздел Разное)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Определяет, является ли автоматическое исправление правописания и отображение орфографические ошибки для выбранной фигуры. Получает логическое значение.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814301"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="205cb-104">Без проверки ячейки (раздел Разное)</span><span class="sxs-lookup"><span data-stu-id="205cb-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="205cb-105">Определяет, является ли автоматическое исправление правописания и отображение орфографические ошибки для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="205cb-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="205cb-106">Получает **логическое** значение.</span><span class="sxs-lookup"><span data-stu-id="205cb-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="205cb-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="205cb-107">**Value**</span></span>|<span data-ttu-id="205cb-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="205cb-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="205cb-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="205cb-109">TRUE</span></span>  <br/> |<span data-ttu-id="205cb-110">Правописания не исправляются автоматически и орфографические ошибки, не отображаются для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="205cb-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="205cb-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="205cb-111">FALSE</span></span>  <br/> |<span data-ttu-id="205cb-112">Автоматическое исправление правописания и орфографические ошибки, отображаются для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="205cb-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="205cb-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="205cb-113">Remarks</span></span>

<span data-ttu-id="205cb-114">Чтобы получить ссылку на ячейку без проверки по имени из другой формулы и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="205cb-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="205cb-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="205cb-115">Cell name:</span></span>  <br/> |<span data-ttu-id="205cb-116">Без проверки</span><span class="sxs-lookup"><span data-stu-id="205cb-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="205cb-117">Для получения ссылки на ячейки без проверки с индекса из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="205cb-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="205cb-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="205cb-118">Section index:</span></span>  <br/> |<span data-ttu-id="205cb-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="205cb-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="205cb-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="205cb-120">Row index:</span></span>  <br/> |<span data-ttu-id="205cb-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="205cb-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="205cb-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="205cb-122">Cell index:</span></span>  <br/> |<span data-ttu-id="205cb-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="205cb-123">**visObjNoProofing**</span></span> <br/> |
   

