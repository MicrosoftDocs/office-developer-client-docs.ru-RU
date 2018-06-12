---
title: Ячейка NoCoauth (раздел свойств документа)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Задает ли документ, хранящийся на сервере Microsoft SharePoint 2013 или Microsoft OneDrive можно редактировать несколькими авторами одновременно в также сеанса.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814302"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="8d8ad-103">Ячейка NoCoauth (раздел свойств документа)</span><span class="sxs-lookup"><span data-stu-id="8d8ad-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="8d8ad-104">Задает ли документ, хранящийся на сервере Microsoft SharePoint 2013 или Microsoft OneDrive можно редактировать несколькими авторами одновременно в также сеанса.</span><span class="sxs-lookup"><span data-stu-id="8d8ad-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="8d8ad-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8d8ad-105">**Value**</span></span>|<span data-ttu-id="8d8ad-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8d8ad-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d8ad-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8d8ad-107">TRUE</span></span>  <br/> |<span data-ttu-id="8d8ad-108">Документ нельзя совместное редактирование и заблокирован для редактирования при открытии.</span><span class="sxs-lookup"><span data-stu-id="8d8ad-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="8d8ad-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8d8ad-109">FALSE</span></span>  <br/> |<span data-ttu-id="8d8ad-110">Можно совместное редактирование документа.</span><span class="sxs-lookup"><span data-stu-id="8d8ad-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d8ad-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="8d8ad-111">Remarks</span></span>

<span data-ttu-id="8d8ad-112">Для получения ссылки на ячейки **NoCoauth** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="8d8ad-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8d8ad-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8d8ad-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8d8ad-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="8d8ad-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="8d8ad-115">Для получения ссылки на ячейки **NoCoauth** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8d8ad-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8d8ad-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8d8ad-116">Section index:</span></span>  <br/> |<span data-ttu-id="8d8ad-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8d8ad-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8d8ad-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8d8ad-118">Row index:</span></span>  <br/> |<span data-ttu-id="8d8ad-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="8d8ad-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="8d8ad-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8d8ad-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8d8ad-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="8d8ad-121">**visDocNoCoauth**</span></span> <br/> |
   

