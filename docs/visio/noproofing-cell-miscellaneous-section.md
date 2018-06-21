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
ms.lasthandoff: 06/21/2018
ms.locfileid: "19814301"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="0b74d-104">Без проверки ячейки (раздел Разное)</span><span class="sxs-lookup"><span data-stu-id="0b74d-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="0b74d-105">Определяет, является ли автоматическое исправление правописания и отображение орфографические ошибки для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="0b74d-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="0b74d-106">Получает **логическое** значение.</span><span class="sxs-lookup"><span data-stu-id="0b74d-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="0b74d-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0b74d-107">**Value**</span></span>|<span data-ttu-id="0b74d-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0b74d-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b74d-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="0b74d-109">TRUE</span></span>  <br/> |<span data-ttu-id="0b74d-110">Правописания не исправляются автоматически и орфографические ошибки, не отображаются для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="0b74d-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="0b74d-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="0b74d-111">FALSE</span></span>  <br/> |<span data-ttu-id="0b74d-112">Автоматическое исправление правописания и орфографические ошибки, отображаются для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="0b74d-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b74d-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="0b74d-113">Remarks</span></span>

<span data-ttu-id="0b74d-114">Чтобы получить ссылку на ячейку без проверки по имени из другой формулы и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="0b74d-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b74d-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0b74d-115">Cell name:</span></span>  <br/> |<span data-ttu-id="0b74d-116">Без проверки</span><span class="sxs-lookup"><span data-stu-id="0b74d-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="0b74d-117">Для получения ссылки на ячейки без проверки с индекса из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0b74d-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b74d-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0b74d-118">Section index:</span></span>  <br/> |<span data-ttu-id="0b74d-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0b74d-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0b74d-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0b74d-120">Row index:</span></span>  <br/> |<span data-ttu-id="0b74d-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="0b74d-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="0b74d-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0b74d-122">Cell index:</span></span>  <br/> |<span data-ttu-id="0b74d-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="0b74d-123">**visObjNoProofing**</span></span> <br/> |
   

