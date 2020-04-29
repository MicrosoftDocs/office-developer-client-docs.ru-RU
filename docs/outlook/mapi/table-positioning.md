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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418591"
---
# <a name="table-positioning"></a><span data-ttu-id="b767a-103">Позиционирование таблицы</span><span class="sxs-lookup"><span data-stu-id="b767a-103">Table Positioning</span></span>

  
  
<span data-ttu-id="b767a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b767a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b767a-105">Текущая позиция в таблице всегда указывается курсором.</span><span class="sxs-lookup"><span data-stu-id="b767a-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="b767a-106">Для каждого представления таблицы существует один курсор; его значение задается средством реализации таблицы.</span><span class="sxs-lookup"><span data-stu-id="b767a-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="b767a-107">Когда клиент или поставщик услуг, использующий таблицу, выдает запрос на изменение позиции таблицы, значение курсора сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="b767a-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="b767a-108">Положение таблицы можно изменить с помощью следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="b767a-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="b767a-109">Закладка.</span><span class="sxs-lookup"><span data-stu-id="b767a-109">A bookmark.</span></span>
    
- <span data-ttu-id="b767a-110">Дробное значение.</span><span class="sxs-lookup"><span data-stu-id="b767a-110">A fractional value.</span></span>
    
- <span data-ttu-id="b767a-111">Фильтр.</span><span class="sxs-lookup"><span data-stu-id="b767a-111">A filter.</span></span>
    

