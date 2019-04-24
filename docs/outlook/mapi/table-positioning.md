---
title: Позиционирование таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 656f696c58e9b62e7e601d7f531870b8c385e862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345656"
---
# <a name="table-positioning"></a><span data-ttu-id="5446c-103">Позиционирование таблицы</span><span class="sxs-lookup"><span data-stu-id="5446c-103">Table Positioning</span></span>

  
  
<span data-ttu-id="5446c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5446c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5446c-105">Текущая позиция в таблице всегда указывается курсором.</span><span class="sxs-lookup"><span data-stu-id="5446c-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="5446c-106">Для каждого представления таблицы существует один курсор; его значение задается средством реализации таблицы.</span><span class="sxs-lookup"><span data-stu-id="5446c-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="5446c-107">Когда клиент или поставщик услуг, использующий таблицу, выдает запрос на изменение позиции таблицы, значение курсора сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="5446c-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="5446c-108">Положение таблицы можно изменить с помощью следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="5446c-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="5446c-109">Закладка.</span><span class="sxs-lookup"><span data-stu-id="5446c-109">A bookmark.</span></span>
    
- <span data-ttu-id="5446c-110">Дробное значение.</span><span class="sxs-lookup"><span data-stu-id="5446c-110">A fractional value.</span></span>
    
- <span data-ttu-id="5446c-111">Фильтр.</span><span class="sxs-lookup"><span data-stu-id="5446c-111">A filter.</span></span>
    

