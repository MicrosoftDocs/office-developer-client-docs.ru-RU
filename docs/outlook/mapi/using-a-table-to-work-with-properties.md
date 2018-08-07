---
title: Работа со свойствами при помощи таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812566"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="c03d9-103">Работа со свойствами при помощи таблицы</span><span class="sxs-lookup"><span data-stu-id="c03d9-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="c03d9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c03d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c03d9-105">Многие свойства доступны из объектов, которые поддерживают их и как столбцы в таблицах.</span><span class="sxs-lookup"><span data-stu-id="c03d9-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="c03d9-106">По возможности получения этих свойств с помощью таблицы.</span><span class="sxs-lookup"><span data-stu-id="c03d9-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="c03d9-107">Вызов [IMAPITable::SetColumns](imapitable-setcolumns.md) для включения всех свойств, которые ваш клиент должен и [IMAPITable::QueryRows](imapitable-queryrows.md) получить все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="c03d9-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="c03d9-108">Эти два звонка обычно подходят для извлечения достаточно сведений для отображения пользователю и часто достаточно для любые необходимые внутренней обработки вызовов **OpenEntry** для открытия ненужных объектов.</span><span class="sxs-lookup"><span data-stu-id="c03d9-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="c03d9-109">Существует только два исключения:</span><span class="sxs-lookup"><span data-stu-id="c03d9-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="c03d9-110">Если свойство не более 255 байт.</span><span class="sxs-lookup"><span data-stu-id="c03d9-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="c03d9-111">** IMAPITable ** интерфейса не может возвращать значение свойства всей, вместо этого усечение до 255 байт.</span><span class="sxs-lookup"><span data-stu-id="c03d9-111">The ** IMAPITable ** interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="c03d9-112">Тем не менее подумайте о задать это соотношение.</span><span class="sxs-lookup"><span data-stu-id="c03d9-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="c03d9-113">При отображении эти данные для пользователя, 255 байт может быть достаточно для текстовых полей, например комментария.</span><span class="sxs-lookup"><span data-stu-id="c03d9-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="c03d9-114">Если вам требуется определенное свойство из одной строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="c03d9-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="c03d9-115">В этом случае не требуется для создания таблицы с помощью свойства, которые никогда не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="c03d9-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="c03d9-116">В большинстве случаев потребуется те же свойства для всех строк.</span><span class="sxs-lookup"><span data-stu-id="c03d9-116">Most of the time you will need the same properties for all rows.</span></span>
    

