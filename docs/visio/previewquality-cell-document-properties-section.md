---
title: Ячейка PreviewQuality (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Определяет, является ли образца документа черновиков качество или подробное.
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814461"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="d0ab0-103">Ячейка PreviewQuality (раздел "Свойства документа")</span><span class="sxs-lookup"><span data-stu-id="d0ab0-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="d0ab0-104">Определяет, является ли образца документа черновиков качество или подробное.</span><span class="sxs-lookup"><span data-stu-id="d0ab0-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="d0ab0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d0ab0-105">**Value**</span></span>|<span data-ttu-id="d0ab0-106">**Качество предварительного просмотра**</span><span class="sxs-lookup"><span data-stu-id="d0ab0-106">**Preview quality**</span></span>|<span data-ttu-id="d0ab0-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="d0ab0-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d0ab0-108">0</span><span class="sxs-lookup"><span data-stu-id="d0ab0-108">0</span></span>  <br/> | <span data-ttu-id="d0ab0-109">Черновик</span><span class="sxs-lookup"><span data-stu-id="d0ab0-109">Draft</span></span>  <br/> |<span data-ttu-id="d0ab0-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="d0ab0-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="d0ab0-111">1</span><span class="sxs-lookup"><span data-stu-id="d0ab0-111">1</span></span>  <br/> | <span data-ttu-id="d0ab0-112">Detailed</span><span class="sxs-lookup"><span data-stu-id="d0ab0-112">Detailed</span></span>  <br/> |<span data-ttu-id="d0ab0-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="d0ab0-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0ab0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d0ab0-114">Remarks</span></span>

<span data-ttu-id="d0ab0-115">Это значение также можно настроить на вкладке **Обзор** в диалоговом окне **Свойства** (нажмите кнопку **Office** , перейдите на вкладку **сведения** , нажмите кнопку **Свойства документа**и выберите команду **Дополнительные свойства**).</span><span class="sxs-lookup"><span data-stu-id="d0ab0-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="d0ab0-116">Чтобы получить ссылку на ячейку PreviewQuality по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d0ab0-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0ab0-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d0ab0-117">Cell name:</span></span>  <br/> | <span data-ttu-id="d0ab0-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="d0ab0-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="d0ab0-119">Для получения ссылки на ячейки PreviewQuality по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d0ab0-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0ab0-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d0ab0-120">Section index:</span></span>  <br/> |<span data-ttu-id="d0ab0-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d0ab0-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d0ab0-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d0ab0-122">Row index:</span></span>  <br/> |<span data-ttu-id="d0ab0-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="d0ab0-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="d0ab0-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d0ab0-124">Cell index:</span></span>  <br/> |<span data-ttu-id="d0ab0-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="d0ab0-125">**visDocPreviewQuality**</span></span> <br/> |
   

