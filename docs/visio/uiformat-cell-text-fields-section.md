---
title: Ячейка UIFormat (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Определяет формат вставленного поля в версии Visio, предшествующие Visio 2000.
ms.openlocfilehash: e9506404e8ccd6ae4452c10ecdcce2d4dfd7ac2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815117"
---
# <a name="uiformat-cell-text-fields-section"></a><span data-ttu-id="279b2-103">Ячейка UIFormat (раздел "Текстовые поля")</span><span class="sxs-lookup"><span data-stu-id="279b2-103">UIFormat Cell (Text Fields Section)</span></span>

<span data-ttu-id="279b2-104">Определяет формат вставленного поля в версии Visio, предшествующие Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="279b2-104">Determines the format of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="279b2-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="279b2-105">Remarks</span></span>

<span data-ttu-id="279b2-106">В этой ячейке не отображается в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="279b2-106">This cell does not appear in the ShapeSheet window.</span></span> <span data-ttu-id="279b2-107">Используйте эту ячейку, если вам потребуется работать с возможностью обратной проблем, таких как сохранение версии 2000 документ Visio в формат файлов Visio версии 5.0.</span><span class="sxs-lookup"><span data-stu-id="279b2-107">Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="279b2-108">Чтобы получить ссылку на ячейку UIFormat по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="279b2-108">To get a reference to the UIFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="279b2-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="279b2-109">Cell name:</span></span>  <br/> | <span data-ttu-id="279b2-110">Fields.UIFmt [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="279b2-110">Fields.UIFmt[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="279b2-111">Для получения ссылки на ячейки UIFormat по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="279b2-111">To get a reference to the UIFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="279b2-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="279b2-112">Section index:</span></span>  <br/> |<span data-ttu-id="279b2-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="279b2-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="279b2-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="279b2-114">Row index:</span></span>  <br/> |<span data-ttu-id="279b2-115">**visRowField** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="279b2-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="279b2-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="279b2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="279b2-117">**visFieldUIFormat**</span><span class="sxs-lookup"><span data-stu-id="279b2-117">**visFieldUIFormat**</span></span> <br/> |
   

