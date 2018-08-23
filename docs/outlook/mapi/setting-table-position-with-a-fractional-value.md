---
title: Установка положения таблицы с использованием дробного значения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8ffed8070c219e6611aebbcb1dd5cd181b662850
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579699"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="64c6a-103">Установка положения таблицы с использованием дробного значения</span><span class="sxs-lookup"><span data-stu-id="64c6a-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="64c6a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64c6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64c6a-105">В таблице пользователи могут перемещаться в позицию, представляющий приблизительно, например процент строк при использовании Общая.</span><span class="sxs-lookup"><span data-stu-id="64c6a-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="64c6a-106">Вместо перемещения в точной строки, этот метод размещения разделяет таблицы в части на основе доли.</span><span class="sxs-lookup"><span data-stu-id="64c6a-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="64c6a-107">В таблице пользователи могут переместить, например точка наполовину способ таблицы или строку, в которой — 7 и 8 способ из таблицы.</span><span class="sxs-lookup"><span data-stu-id="64c6a-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="64c6a-108">**Перемещение курсора приблизительное число строк**</span><span class="sxs-lookup"><span data-stu-id="64c6a-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="64c6a-109">Вызов [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="64c6a-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="64c6a-110">**SeekRowApprox** перемещает строку, представляющую определенный процент строк при использовании начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="64c6a-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="64c6a-111">Этот процент указано в параметрах _ulNumerator_ и _ulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="64c6a-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="64c6a-112">**SeekRowApprox** часто используется для реализации полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="64c6a-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="64c6a-113">**Чтобы определить, приблизительно, например положение таблицы**</span><span class="sxs-lookup"><span data-stu-id="64c6a-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="64c6a-114">Вызов [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="64c6a-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="64c6a-115">**QueryPosition** можно использовать для оповещения пользователя о текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="64c6a-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="64c6a-116">Задает дробное значение на основе номер текущей строки и число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="64c6a-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="64c6a-117">Ожидается, что это значение представляет приблизительным.</span><span class="sxs-lookup"><span data-stu-id="64c6a-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="64c6a-118">В таблице специалистов по внедрению, рекомендуется не для вычисления точное положение, поскольку точных реализации может быть дорогим для вызова, особенно в таблицах по категориям.</span><span class="sxs-lookup"><span data-stu-id="64c6a-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="64c6a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="64c6a-119">See also</span></span>



[<span data-ttu-id="64c6a-120">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="64c6a-120">MAPI Tables</span></span>](mapi-tables.md)

