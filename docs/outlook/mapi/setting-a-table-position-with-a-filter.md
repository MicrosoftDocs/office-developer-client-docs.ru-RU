---
title: Настройка позиции таблицы с помощью фильтра
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425472"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="9c089-103">Настройка позиции таблицы с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="9c089-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="9c089-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c089-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c089-105">Пользователи таблицы могут переместить курсор в строку, которая соответствует набору критериев фильтрации.</span><span class="sxs-lookup"><span data-stu-id="9c089-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="9c089-106">Фильтры могут быть основаны на различных рекомендациях, таких как значения свойств столбцов, битмаски или подобекты.</span><span class="sxs-lookup"><span data-stu-id="9c089-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="9c089-107">Фильтры указаны в MAPI с помощью [структуры SRestriction.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="9c089-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="9c089-108">**Расположение таблицы к первой строке, которая соответствует критериям, установленным в ограничении**</span><span class="sxs-lookup"><span data-stu-id="9c089-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="9c089-109">Вызов метода [IMAPITable::FindRow.](imapitable-findrow.md)</span><span class="sxs-lookup"><span data-stu-id="9c089-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="9c089-110">Начиная со строки, представленной определенной закладкой, **FindRow** выполняет поиск в направлении вперед или назад, чтобы найти строку, которая соответствует критериям, указанным в ограничении.</span><span class="sxs-lookup"><span data-stu-id="9c089-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="9c089-111">**FindRow** может быть полезен для реализации панели прокрутки, основанной на строках символов, а не на дробных значениях.</span><span class="sxs-lookup"><span data-stu-id="9c089-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="9c089-112">Например, клиент может вызвать реализацию **MapI FindRow** при поиске через интегрированную адресную книгу, чтобы пользователь, введите один или несколько символов, найти имя, которое начинается с указанных символов.</span><span class="sxs-lookup"><span data-stu-id="9c089-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9c089-113">См. также</span><span class="sxs-lookup"><span data-stu-id="9c089-113">See also</span></span>



[<span data-ttu-id="9c089-114">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="9c089-114">MAPI Tables</span></span>](mapi-tables.md)

