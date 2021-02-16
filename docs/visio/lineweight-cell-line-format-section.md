---
title: LineWeight Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Определяет вес линии фигуры. Установите вес линии, введите номер с допустимой единицей измерения.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412249"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="bbdfd-104">LineWeight Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="bbdfd-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="bbdfd-105">Определяет вес линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="bbdfd-105">Determines the line weight of a shape.</span></span> <span data-ttu-id="bbdfd-106">Установите вес линии, введите номер с допустимой единицей измерения.</span><span class="sxs-lookup"><span data-stu-id="bbdfd-106">Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bbdfd-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="bbdfd-107">Remarks</span></span>

<span data-ttu-id="bbdfd-108">Вы также можете установить значение LineWeight в диалоговом  окне  **"Линия"** (на вкладке "Главная" в группе "Фигура" щелкните **"Строка"** и "Вес" **и** выберите "Дополнительные **строки").**</span><span class="sxs-lookup"><span data-stu-id="bbdfd-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="bbdfd-109">Если единица измерения не введена, используется единица измерения для текста, указанного в диалоговом окне "Параметры **Visio"** (щелкните вкладку "Файл" и выберите **"Параметры").** </span><span class="sxs-lookup"><span data-stu-id="bbdfd-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="bbdfd-110">Вес линии не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="bbdfd-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="bbdfd-111">При масштабе рисования вес линии остается таким же.</span><span class="sxs-lookup"><span data-stu-id="bbdfd-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="bbdfd-112">Чтобы получить ссылку на ячейку LineWeight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="bbdfd-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bbdfd-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bbdfd-113">Cell name:</span></span>  <br/> | <span data-ttu-id="bbdfd-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="bbdfd-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="bbdfd-115">Чтобы получить ссылку на ячейку LineWeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bbdfd-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bbdfd-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bbdfd-116">Section index:</span></span>  <br/> |<span data-ttu-id="bbdfd-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bbdfd-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bbdfd-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bbdfd-118">Row index:</span></span>  <br/> |<span data-ttu-id="bbdfd-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="bbdfd-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="bbdfd-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bbdfd-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bbdfd-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="bbdfd-121">**visLineWeight**</span></span> <br/> |
   

