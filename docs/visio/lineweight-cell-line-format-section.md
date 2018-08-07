---
title: Ячейка LineWeight (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Определяет Толщина линии фигуры. Задайте Толщина линии путем ввода цифр с допустимой единицы измерения.
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814093"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="0ab1e-104">Ячейка LineWeight (раздел "Формат линий")</span><span class="sxs-lookup"><span data-stu-id="0ab1e-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="0ab1e-105">Определяет Толщина линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="0ab1e-105">Determines the line weight of a shape.</span></span> <span data-ttu-id="0ab1e-106">Задайте Толщина линии путем ввода цифр с допустимой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="0ab1e-106">Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ab1e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="0ab1e-107">Remarks</span></span>

<span data-ttu-id="0ab1e-108">Можно также задать значение Толщина линии в диалоговом окне " **строка** " (на вкладке **Главная** в группе **фигуры** щелкните **строку**, выберите пункт **Вес**и нажмите кнопку **Другие линии**).</span><span class="sxs-lookup"><span data-stu-id="0ab1e-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="0ab1e-109">Если единицы измерения не введена, используется единицу измерения для текста, указанного в диалоговом окне **Параметры Visio** (перейдите на вкладку **файл** и выберите пункт **Параметры**).</span><span class="sxs-lookup"><span data-stu-id="0ab1e-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="0ab1e-110">Толщина линии не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="0ab1e-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="0ab1e-111">Если документа изменяется, толщина линии остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="0ab1e-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="0ab1e-112">Для получения ссылки на ячейки Толщина линии по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0ab1e-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ab1e-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0ab1e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="0ab1e-114">Толщина линии</span><span class="sxs-lookup"><span data-stu-id="0ab1e-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="0ab1e-115">Для получения ссылки на ячейки Толщина линии по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0ab1e-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ab1e-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0ab1e-116">Section index:</span></span>  <br/> |<span data-ttu-id="0ab1e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0ab1e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0ab1e-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0ab1e-118">Row index:</span></span>  <br/> |<span data-ttu-id="0ab1e-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="0ab1e-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="0ab1e-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0ab1e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0ab1e-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="0ab1e-121">**visLineWeight**</span></span> <br/> |
   

