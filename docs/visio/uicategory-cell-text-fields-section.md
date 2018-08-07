---
title: Ячейка UICategory (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Определяет категории вставленный поля в версии Visio, предшествующие Visio 2000.
ms.openlocfilehash: fc060ac1533732749d10e1855dc3841602051520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815099"
---
# <a name="uicategory-cell-text-fields-section"></a><span data-ttu-id="d4d6c-103">Ячейка UICategory (раздел "Текстовые поля")</span><span class="sxs-lookup"><span data-stu-id="d4d6c-103">UICategory Cell (Text Fields Section)</span></span>

<span data-ttu-id="d4d6c-104">Определяет категории вставленный поля в версии Visio, предшествующие Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-104">Determines the category of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4d6c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4d6c-105">Remarks</span></span>

<span data-ttu-id="d4d6c-106">В этой ячейке не отображается в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-106">This cell does not appear in the ShapeSheet window.</span></span> <span data-ttu-id="d4d6c-107">Используйте эту ячейку, если вам потребуется работать с обратной возможность проблемы, такие как сохранение версии 2000 документ Visio в формат файлов Visio версии 5.0.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-107">Use this cell if you need to deal with backward capability issues such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="d4d6c-108">Чтобы получить ссылку на ячейку UICategory по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d4d6c-108">To get a reference to the UICategory cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4d6c-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d4d6c-110">Fields.UICat [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d4d6c-110">Fields.UICat[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d4d6c-111">Для получения ссылки на ячейки UICategory по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d4d6c-111">To get a reference to the UICategory cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4d6c-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d4d6c-112">Section index:</span></span>  <br/> |<span data-ttu-id="d4d6c-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="d4d6c-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="d4d6c-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d4d6c-114">Row index:</span></span>  <br/> |<span data-ttu-id="d4d6c-115">**visRowField** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d4d6c-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d4d6c-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d4d6c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d4d6c-117">**visFieldUICategory**</span><span class="sxs-lookup"><span data-stu-id="d4d6c-117">**visFieldUICategory**</span></span> <br/> |
   

