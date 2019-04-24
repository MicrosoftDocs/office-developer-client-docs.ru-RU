---
title: CenterY Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Определяет, будет ли страница документа центрироваться по вертикали на странице принтера.
ms.openlocfilehash: 858bf41c74fdcbd82d271a379df7c5816a7796fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341918"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="b2813-103">CenterY Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="b2813-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="b2813-104">Определяет, будет ли страница документа центрироваться по вертикали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="b2813-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="b2813-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="b2813-105">**Value**</span></span>|<span data-ttu-id="b2813-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b2813-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b2813-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2813-107">TRUE</span></span>  <br/> | <span data-ttu-id="b2813-108">РазЦентрирование страницы документа по вертикали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="b2813-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="b2813-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b2813-109">FALSE</span></span>  <br/> | <span data-ttu-id="b2813-110">Не выравнивать страницу документа по вертикали на странице принтера (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b2813-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2813-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2813-111">Remarks</span></span>

<span data-ttu-id="b2813-112">По умолчанию страницы документа выравниваются по верхнему и левому краю страницы принтера.</span><span class="sxs-lookup"><span data-stu-id="b2813-112">By default, drawing pages are justified to the top and left of the printer page.</span></span> <span data-ttu-id="b2813-113">Установка для CenterX и центрированных ячеек значения TRUE поместит страницу документа в центре страницы принтера (или на страницах при необходимости заполнения).</span><span class="sxs-lookup"><span data-stu-id="b2813-113">Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="b2813-114">Чтобы получить ссылку на центральную ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b2813-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2813-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b2813-115">Cell name:</span></span>  <br/> | <span data-ttu-id="b2813-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="b2813-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="b2813-117">Чтобы получить ссылку на центральную ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b2813-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2813-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b2813-118">Section index:</span></span>  <br/> |<span data-ttu-id="b2813-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b2813-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b2813-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b2813-120">Row index:</span></span>  <br/> |<span data-ttu-id="b2813-121">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="b2813-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="b2813-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b2813-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b2813-123">**Виспринтпропертиесцентери**</span><span class="sxs-lookup"><span data-stu-id="b2813-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

