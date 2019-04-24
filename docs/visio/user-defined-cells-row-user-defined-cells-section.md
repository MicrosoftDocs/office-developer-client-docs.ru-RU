---
title: User-defined Cells Row (User-defined Cells Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Содержит значение и описательное приглашение для всех ячеек в решении, определенных пользователем. Фигура содержит одну строку заданных пользователем ячеек для каждой из заданных пользователем комбинаций ячеек значений и приглашений.
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337186"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a><span data-ttu-id="85325-104">User-defined Cells Row (User-defined Cells Section)</span><span class="sxs-lookup"><span data-stu-id="85325-104">User-defined Cells Row (User-defined Cells Section)</span></span>

<span data-ttu-id="85325-105">Содержит значение и описательное приглашение для всех ячеек в решении, определенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="85325-105">Contains the value and descriptive prompt for any user-defined cells in your solution.</span></span> <span data-ttu-id="85325-106">Фигура содержит одну строку заданных пользователем ячеек для каждой из заданных пользователем комбинаций ячеек значений и приглашений.</span><span class="sxs-lookup"><span data-stu-id="85325-106">A shape contains one User-defined Cells row for each user-defined Value/Prompt cell pair.</span></span>
  
<span data-ttu-id="85325-107">Строки с пользовательскими ячейками называются User.</span><span class="sxs-lookup"><span data-stu-id="85325-107">User-defined Cells rows are named User.</span></span> <span data-ttu-id="85325-108">*имя* и содержит следующие ячейки.</span><span class="sxs-lookup"><span data-stu-id="85325-108">*name*  and contain the following cells.</span></span> <span data-ttu-id="85325-109">Более подробную информацию можно найти в разделах, посвященных определенным ячейкам.</span><span class="sxs-lookup"><span data-stu-id="85325-109">For more details, see the specific cell topics.</span></span> 
  
|<span data-ttu-id="85325-110">**Cell**</span><span class="sxs-lookup"><span data-stu-id="85325-110">**Cell**</span></span>|<span data-ttu-id="85325-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="85325-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85325-112">Значение</span><span class="sxs-lookup"><span data-stu-id="85325-112">Value</span></span>](value-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="85325-113">Задает значение для соответствующей пользовательской ячейки.</span><span class="sxs-lookup"><span data-stu-id="85325-113">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |
|[<span data-ttu-id="85325-114">Prompt</span><span class="sxs-lookup"><span data-stu-id="85325-114">Prompt</span></span>](prompt-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="85325-115">Задает описательное приглашение или комментарий для пользовательской ячейки.</span><span class="sxs-lookup"><span data-stu-id="85325-115">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85325-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85325-116">Remarks</span></span>

<span data-ttu-id="85325-117">Пользовательские ячейки можно использовать для ввода формул или констант, на которые ссылаются другие ячейки или надстройки.</span><span class="sxs-lookup"><span data-stu-id="85325-117">User-defined cells can be used for entering formulas or constants that are referred to by other cells or add-ons.</span></span> <span data-ttu-id="85325-118">Значения в пользовательских ячейках являются переносимыми, то есть если фигура, ссылающаяся на пользовательскую ячейку в одной фигуре, копируется в другую фигуру, которая не имеет той же пользовательской ячейки, ячейка добавляется к фигуре.</span><span class="sxs-lookup"><span data-stu-id="85325-118">Values in user-defined cells are portable, that is, if a shape that refers to a user-defined cell in one shape is copied to another shape that does not have the same user-defined cell, the cell is added to the shape.</span></span>
  
 <span data-ttu-id="85325-119">Можно добавить любое количество пользователей.</span><span class="sxs-lookup"><span data-stu-id="85325-119">You can add as many User.</span></span>  <span data-ttu-id="85325-120">\*\* укажите имена строк, назначьте им значимые имена и задайте значения ячеек.</span><span class="sxs-lookup"><span data-stu-id="85325-120">*name*  rows as you need, assign meaningful names to the rows, and set cell values.</span></span> <span data-ttu-id="85325-121">Чтобы добавить строку в существующий раздел "пользовательские ячейки", щелкните правой кнопкой мыши строку и выберите команду **Вставить строку** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="85325-121">To add a row to an existing User-defined Cells section, right-click a row and click **Insert Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="85325-122">Вы можете ссылаться на эти ячейки по имени строки, которое отображается в окне таблицы свойств фигуры в виде красного текста.</span><span class="sxs-lookup"><span data-stu-id="85325-122">You can reference these cells by their row name, which appears in a ShapeSheet window in red text.</span></span> <span data-ttu-id="85325-123">Для назначения осмысленных имен пользователю.</span><span class="sxs-lookup"><span data-stu-id="85325-123">To assign meaningful names to User.</span></span> <span data-ttu-id="85325-124">*имя* строки, щелкните строку, а затем введите имя (например, *offset* ), например, чтобы создать имя строки User. offset.</span><span class="sxs-lookup"><span data-stu-id="85325-124">*name*  rows, click the row, and then type a name such as  *Offset*  , for example, to create the row name User.Offset.</span></span> <span data-ttu-id="85325-125">Затем вы можете ссылаться на ячейку Prompt с помощью User. offset. prompt.</span><span class="sxs-lookup"><span data-stu-id="85325-125">You can then reference the Prompt cell using User.Offset.Prompt.</span></span> 
  
<span data-ttu-id="85325-126">Введенное имя строки должно быть уникальным в пределах раздела.</span><span class="sxs-lookup"><span data-stu-id="85325-126">The row name you enter must be unique within the section.</span></span>
  

