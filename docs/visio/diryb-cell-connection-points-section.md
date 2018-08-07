---
title: Ячейка DirY / B (раздел "Точки соединения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Определяет, y-компонент для вектор Обязательное выравнивание совпадающих точки подключения. Он также используется для сориентироваться вложенные ветвь динамических соединителя. В этой ячейке принимает число с плавающей запятой.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813594"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="ed0f8-105">Ячейка DirY / B (раздел "Точки соединения")</span><span class="sxs-lookup"><span data-stu-id="ed0f8-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="ed0f8-106">Определяет, *y* -компонент для вектор Обязательное выравнивание совпадающих точки подключения.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="ed0f8-107">Он также используется для сориентироваться вложенные ветвь динамических соединителя.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="ed0f8-108">В этой ячейке принимает число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ed0f8-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="ed0f8-109">Remarks</span></span>

<span data-ttu-id="ed0f8-110">Чтобы получить ссылку на DirY / B ячейки по имени из другой формулы или из файла с помощью свойства **CellsU** , использования:</span><span class="sxs-lookup"><span data-stu-id="ed0f8-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed0f8-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-111">Cell name:</span></span>  <br/> |<span data-ttu-id="ed0f8-112">Connections.DirY [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ed0f8-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ed0f8-113">Чтобы получить ссылку на DirY / B ячейки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ed0f8-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed0f8-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ed0f8-114">Section index:</span></span>  <br/> |<span data-ttu-id="ed0f8-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="ed0f8-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="ed0f8-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ed0f8-116">Row index:</span></span>  <br/> |<span data-ttu-id="ed0f8-117">**visRowConnectionPts** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ed0f8-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="ed0f8-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ed0f8-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ed0f8-119">**visCnnctDirY** (не только строк)           **visCnnctB** (расширенные строк)</span><span class="sxs-lookup"><span data-stu-id="ed0f8-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="ed0f8-120">Сведения о не расширены и расширенного строк, в разделе точек подключения строки.</span><span class="sxs-lookup"><span data-stu-id="ed0f8-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

