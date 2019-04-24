---
title: Задание позиции таблицы с использованием дробного значения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339265"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="ea7ff-103">Задание позиции таблицы с использованием дробного значения</span><span class="sxs-lookup"><span data-stu-id="ea7ff-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="ea7ff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea7ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea7ff-105">Пользователи таблиц могут перемещаться в позицию, представляющую Приблизительный процент строк относительно итогового значения.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="ea7ff-106">Вместо того чтобы перемещаться в точную строку, этот метод размещения разделяет таблицу на части на основе дробей.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="ea7ff-107">Пользователь таблицы может перемещаться, например, в двустороннюю точку таблицы или в строку, которая находится в 7/8 способе прокрутки таблицы.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="ea7ff-108">**Перемещение курсора на приблизительное число строк**</span><span class="sxs-lookup"><span data-stu-id="ea7ff-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="ea7ff-109">Вызов [IMAPITable:: сикроваппрокс](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="ea7ff-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="ea7ff-110">**Сикроваппрокс** перемещается в строку, представляющую определенный процент строк относительно начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="ea7ff-111">Этот процент задается в параметрах _улнумератор_ и _улденоминатор_ .</span><span class="sxs-lookup"><span data-stu-id="ea7ff-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="ea7ff-112">**Сикроваппрокс** часто используется для реализации полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="ea7ff-113">**Определение приблизительного положения таблицы**</span><span class="sxs-lookup"><span data-stu-id="ea7ff-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="ea7ff-114">Вызов [IMAPITable:: куерипоситион](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="ea7ff-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="ea7ff-115">**Куерипоситион** можно использовать для информирования пользователя о текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="ea7ff-116">Он задает дробное значение на основе количества строк в таблице и номера текущей строки.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="ea7ff-117">Ожидается, что это значение представляет собой приближение.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="ea7ff-118">Разработчикам таблиц рекомендуется не вычислять точную позицию, так как точные реализации могут вызывать дорогостоящие затраты, особенно на классифицированных таблицах.</span><span class="sxs-lookup"><span data-stu-id="ea7ff-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ea7ff-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ea7ff-119">See also</span></span>



[<span data-ttu-id="ea7ff-120">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="ea7ff-120">MAPI Tables</span></span>](mapi-tables.md)

