---
title: PreviewQuality Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Определяет, является ли предварительный просмотр изображения черновым или подробным.
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416820"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="6c6b7-103">PreviewQuality Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="6c6b7-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="6c6b7-104">Определяет, является ли предварительный просмотр изображения черновым или подробным.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="6c6b7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6c6b7-105">**Value**</span></span>|<span data-ttu-id="6c6b7-106">**Предварительное качество**</span><span class="sxs-lookup"><span data-stu-id="6c6b7-106">**Preview quality**</span></span>|<span data-ttu-id="6c6b7-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="6c6b7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6c6b7-108">нуль</span><span class="sxs-lookup"><span data-stu-id="6c6b7-108">0</span></span>  <br/> | <span data-ttu-id="6c6b7-109">Черновик</span><span class="sxs-lookup"><span data-stu-id="6c6b7-109">Draft</span></span>  <br/> |<span data-ttu-id="6c6b7-110">**Висдокпревиевкуалитидрафт**</span><span class="sxs-lookup"><span data-stu-id="6c6b7-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="6c6b7-111">1,1</span><span class="sxs-lookup"><span data-stu-id="6c6b7-111">1</span></span>  <br/> | <span data-ttu-id="6c6b7-112">Дроб</span><span class="sxs-lookup"><span data-stu-id="6c6b7-112">Detailed</span></span>  <br/> |<span data-ttu-id="6c6b7-113">**Висдокпревиевкуалитидетаилед**</span><span class="sxs-lookup"><span data-stu-id="6c6b7-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c6b7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c6b7-114">Remarks</span></span>

<span data-ttu-id="6c6b7-115">Это значение можно также задать на вкладке **Сводка** диалогового окна **Свойства** (нажмите кнопку **Office** , перейдите на вкладку **сведения** , щелкните **Свойства документа**, а затем выберите **Дополнительные свойства**).</span><span class="sxs-lookup"><span data-stu-id="6c6b7-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="6c6b7-116">Чтобы получить ссылку на ячейку PreviewQuality по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="6c6b7-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c6b7-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6c6b7-117">Cell name:</span></span>  <br/> | <span data-ttu-id="6c6b7-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="6c6b7-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="6c6b7-119">Чтобы получить ссылку на ячейку PreviewQuality по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6c6b7-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c6b7-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6c6b7-120">Section index:</span></span>  <br/> |<span data-ttu-id="6c6b7-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6c6b7-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6c6b7-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6c6b7-122">Row index:</span></span>  <br/> |<span data-ttu-id="6c6b7-123">**Висровдок**</span><span class="sxs-lookup"><span data-stu-id="6c6b7-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="6c6b7-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6c6b7-124">Cell index:</span></span>  <br/> |<span data-ttu-id="6c6b7-125">**Висдокпревиевкуалити**</span><span class="sxs-lookup"><span data-stu-id="6c6b7-125">**visDocPreviewQuality**</span></span> <br/> |
   

