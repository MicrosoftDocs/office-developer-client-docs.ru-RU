---
title: Установка положения таблицы с использованием фильтра
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565594"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="0ad50-103">Установка положения таблицы с использованием фильтра</span><span class="sxs-lookup"><span data-stu-id="0ad50-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="0ad50-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ad50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ad50-105">Пользователи могут переместите курсор к строку, которая соответствует набор условий фильтра.</span><span class="sxs-lookup"><span data-stu-id="0ad50-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="0ad50-106">Фильтры может быть основана на ряд рекомендаций, например, значения свойств столбца, битовой маски или вложенных объектов.</span><span class="sxs-lookup"><span data-stu-id="0ad50-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="0ad50-107">Фильтры указаны в MAPI, с помощью структуры [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad50-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="0ad50-108">**Для размещения таблицы в первую строку, которая соответствует критериям, приведенным в качестве ограничения**</span><span class="sxs-lookup"><span data-stu-id="0ad50-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="0ad50-109">Вызовите метод [IMAPITable::FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad50-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="0ad50-110">Начиная с строки, представленной определенную закладку **FindRow** осуществляет поиск в прямом или обратном направлении найдите строку, которая соответствует условиям, указанного в ограничении.</span><span class="sxs-lookup"><span data-stu-id="0ad50-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="0ad50-111">Можно использовать для реализации полосу прокрутки, основанный на строк символов, а не дробной **FindRow** .</span><span class="sxs-lookup"><span data-stu-id="0ad50-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="0ad50-112">Например клиент может вызвать реализацию MAPI's **FindRow** при поиске по интегрированной адресной книги, чтобы включить для пользователя, указав один или несколько знаков, чтобы найти имя, которое начинается с указанных символов.</span><span class="sxs-lookup"><span data-stu-id="0ad50-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0ad50-113">См. также</span><span class="sxs-lookup"><span data-stu-id="0ad50-113">See also</span></span>



[<span data-ttu-id="0ad50-114">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="0ad50-114">MAPI Tables</span></span>](mapi-tables.md)

