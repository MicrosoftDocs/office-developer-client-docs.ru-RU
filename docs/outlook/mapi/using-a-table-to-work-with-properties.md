---
title: Использование таблицы для работы со свойствами
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
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="fdeec-103">Использование таблицы для работы со свойствами</span><span class="sxs-lookup"><span data-stu-id="fdeec-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="fdeec-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdeec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdeec-105">Многие свойства доступны как из объектов, которые их поддерживают, так и в виде столбцов в таблицах.</span><span class="sxs-lookup"><span data-stu-id="fdeec-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="fdeec-106">Когда это возможно, извлеките эти свойства через таблицу.</span><span class="sxs-lookup"><span data-stu-id="fdeec-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="fdeec-107">Call [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) , чтобы включить все свойства, необходимые для клиента, и [IMAPITable:: QueryRows](imapitable-queryrows.md) , чтобы получить все строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="fdeec-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="fdeec-108">Эти два вызова обычно достаточно подходят для получения достаточной информации для отображения пользователю и, как правило, достаточно для любой необходимой внутренней обработки, делая вызов **OpenEntry** для открытия объекта ненужным.</span><span class="sxs-lookup"><span data-stu-id="fdeec-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="fdeec-109">Существует только два исключения.</span><span class="sxs-lookup"><span data-stu-id="fdeec-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="fdeec-110">, Если свойство превышает 255 байт.</span><span class="sxs-lookup"><span data-stu-id="fdeec-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="fdeec-111">Интерфейс \* \* IMAPITable \* \* может не возвращать значение свойства целиком, а отбрасывает его в 255 байт.</span><span class="sxs-lookup"><span data-stu-id="fdeec-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="fdeec-112">Тем не менее, подумайте об этом компромиссе.</span><span class="sxs-lookup"><span data-stu-id="fdeec-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="fdeec-113">Если вы отображаете эти данные для пользователя, 255 байт могут быть достаточно для текстового поля, например комментария.</span><span class="sxs-lookup"><span data-stu-id="fdeec-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="fdeec-114">Если требуется определенное свойство из одной строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="fdeec-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="fdeec-115">В этом случае нет необходимости создавать таблицу со свойствами, которые никогда не будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="fdeec-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="fdeec-116">В большинстве случаев для всех строк потребуется одинаковое свойство.</span><span class="sxs-lookup"><span data-stu-id="fdeec-116">Most of the time you will need the same properties for all rows.</span></span>
    

