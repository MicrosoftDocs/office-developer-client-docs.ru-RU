---
title: Использование таблицы для работы с свойствами
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439914"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="50a67-103">Использование таблицы для работы с свойствами</span><span class="sxs-lookup"><span data-stu-id="50a67-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="50a67-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50a67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50a67-105">Многие свойства доступны как из поддерживаемых объектов, так и в качестве столбцов на столах.</span><span class="sxs-lookup"><span data-stu-id="50a67-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="50a67-106">По возможности извлекай эти свойства через таблицу.</span><span class="sxs-lookup"><span data-stu-id="50a67-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="50a67-107">Вызов [IMAPITable::SetColumns,](imapitable-setcolumns.md) чтобы включить все свойства, необходимые клиенту, и [IMAPITable::QueryRows,](imapitable-queryrows.md) чтобы получить все строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="50a67-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="50a67-108">Эти два вызова обычно достаточны для получения достаточного количества сведений для отображения пользователю и часто являются достаточными для любой необходимой внутренней обработки, что делает вызов **в OpenEntry,** чтобы открыть объект ненужным.</span><span class="sxs-lookup"><span data-stu-id="50a67-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="50a67-109">Существует только два исключения:</span><span class="sxs-lookup"><span data-stu-id="50a67-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="50a67-110">Если свойство более 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="50a67-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="50a67-111">Интерфейс IMAPITable \*\* может не возвращать все значение свойства, а усеченный на 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="50a67-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="50a67-112">Однако подумайте об этом компромиссе.</span><span class="sxs-lookup"><span data-stu-id="50a67-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="50a67-113">Если вы отображаете эти данные пользователю, для текстового поля, например комментария, может хватить 255 битов.</span><span class="sxs-lookup"><span data-stu-id="50a67-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="50a67-114">Если вам нужно определенное свойство из одной строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="50a67-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="50a67-115">В этом случае нет необходимости создавать таблицу со свойствами, которые никогда не будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="50a67-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="50a67-116">В большинстве раз вам потребуется одно и то же свойства для всех строк.</span><span class="sxs-lookup"><span data-stu-id="50a67-116">Most of the time you will need the same properties for all rows.</span></span>
    

