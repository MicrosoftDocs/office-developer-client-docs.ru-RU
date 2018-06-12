---
title: Ячейка UICode (текстовые поля, раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Определяет код, вставленный поля в версии Visio, предшествующие Visio 2000.
ms.openlocfilehash: ce05f779bfebd5720555f1a2d92b1f9f92cfbdfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815094"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="1b706-103">Ячейка UICode (текстовые поля, раздел)</span><span class="sxs-lookup"><span data-stu-id="1b706-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="1b706-104">Определяет код, вставленный поля в версии Visio, предшествующие Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="1b706-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b706-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b706-105">Remarks</span></span>

<span data-ttu-id="1b706-106">В этой ячейке не отображается в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="1b706-106">This cell does not appear in the ShapeSheet window.</span></span> <span data-ttu-id="1b706-107">Используйте эту ячейку, если вам потребуется работать с возможностью обратной проблем, таких как сохранение версии 2000 документ Visio в формат файлов Visio версии 5.0.</span><span class="sxs-lookup"><span data-stu-id="1b706-107">Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="1b706-108">Чтобы получить ссылку на ячейку UICode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1b706-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b706-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="1b706-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1b706-110">Fields.UICod [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1b706-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1b706-111">Для получения ссылки на ячейки UICode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="1b706-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b706-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1b706-112">Section index:</span></span>  <br/> |<span data-ttu-id="1b706-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="1b706-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="1b706-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1b706-114">Row index:</span></span>  <br/> |<span data-ttu-id="1b706-115">**visRowField** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1b706-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1b706-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1b706-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1b706-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="1b706-117">**visFieldUICode**</span></span> <br/> |
   

