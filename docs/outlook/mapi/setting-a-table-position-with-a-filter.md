---
title: Установка позиции таблицы с помощью фильтра
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
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="e22fb-103">Установка позиции таблицы с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="e22fb-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="e22fb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e22fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e22fb-105">Таблица пользователи могут перемещать курсор в строку, которая соответствует набору условий фильтра.</span><span class="sxs-lookup"><span data-stu-id="e22fb-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="e22fb-106">Фильтры могут основываться на различных рекомендациях, таких как значения свойств столбцов, битовые маски или подобъекты.</span><span class="sxs-lookup"><span data-stu-id="e22fb-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="e22fb-107">Фильтры указываются в MAPI с использованием структуры [срестриктион](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="e22fb-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="e22fb-108">**Размещение таблицы в первую строку, которая соответствует критериям, установленным в ограничении**</span><span class="sxs-lookup"><span data-stu-id="e22fb-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="e22fb-109">ВыЗовите метод [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="e22fb-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="e22fb-110">Начиная со строки, представленной определенной закладкой, **FindRow** ищет строку, которая соответствует критериям, указанным в ограничении, в перенаправлении вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="e22fb-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="e22fb-111">**FindRow** может быть полезен для реализации полосы прокрутки на основе символьных строк, а не дробных значений.</span><span class="sxs-lookup"><span data-stu-id="e22fb-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="e22fb-112">Например, клиент может вызвать метод **FindRow** интерфейса MAPI при поиске пользователя с помощью встроенной адресной книги, чтобы включить пользователя, указав один или несколько символов, чтобы найти первое имя, начинающееся с указанных символов.</span><span class="sxs-lookup"><span data-stu-id="e22fb-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e22fb-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e22fb-113">See also</span></span>



[<span data-ttu-id="e22fb-114">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="e22fb-114">MAPI Tables</span></span>](mapi-tables.md)

