---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Определяет, может ли документ, хранимый на сервере Microsoft SharePoint 2013 или Microsoft OneDrive, одновременно редактироваться несколькими авторами в сеансе совместной работы.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420516"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="9b10f-103">NoCoauth Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="9b10f-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="9b10f-104">Определяет, может ли документ, хранимый на сервере Microsoft SharePoint 2013 или Microsoft OneDrive, одновременно редактироваться несколькими авторами в сеансе совместной работы.</span><span class="sxs-lookup"><span data-stu-id="9b10f-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="9b10f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9b10f-105">**Value**</span></span>|<span data-ttu-id="9b10f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9b10f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b10f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9b10f-107">TRUE</span></span>  <br/> |<span data-ttu-id="9b10f-108">Документ не может быть соавтором и заблокирован для редактирования при его открытом режиме.</span><span class="sxs-lookup"><span data-stu-id="9b10f-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="9b10f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9b10f-109">FALSE</span></span>  <br/> |<span data-ttu-id="9b10f-110">Документ можно совместно использовать.</span><span class="sxs-lookup"><span data-stu-id="9b10f-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b10f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b10f-111">Remarks</span></span>

<span data-ttu-id="9b10f-112">Чтобы получить ссылку на ячейку **NoCoauth** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="9b10f-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b10f-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9b10f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9b10f-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="9b10f-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="9b10f-115">Чтобы получить ссылку на ячейку **NoCoauth** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9b10f-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b10f-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9b10f-116">Section index:</span></span>  <br/> |<span data-ttu-id="9b10f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9b10f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9b10f-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9b10f-118">Row index:</span></span>  <br/> |<span data-ttu-id="9b10f-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="9b10f-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="9b10f-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9b10f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9b10f-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="9b10f-121">**visDocNoCoauth**</span></span> <br/> |
   

