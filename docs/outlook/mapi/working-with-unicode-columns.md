---
title: Работа со столбцами в Юникоде
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325573"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="a95b2-103">Работа со столбцами в Юникоде</span><span class="sxs-lookup"><span data-stu-id="a95b2-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="a95b2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a95b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a95b2-105">Строки символов в таблицах могут быть представлены с помощью стандартных 8 – разрядных символов, которые представляют собой тип свойства PT_STRING8, или 16 – битовые знаки Юникода, которые являются типом свойства ПТ_УНИКОДЕ.</span><span class="sxs-lookup"><span data-stu-id="a95b2-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="a95b2-106">Разработчики таблиц могут свободно выбирать, могут ли их таблицы поддерживать строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="a95b2-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="a95b2-107">Так как Юникод добавляет значение для клиентов и поставщиков услуг, расширяя набор функций, везде, где это возможно, рекомендуется поддерживать Юникод.</span><span class="sxs-lookup"><span data-stu-id="a95b2-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="a95b2-108">Многие методы таблиц принимают флаг, определяющий, должны ли значения свойства String быть Юникод.</span><span class="sxs-lookup"><span data-stu-id="a95b2-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="a95b2-109">При вводе при указании флага МАПИ_УНИКОДЕ значение, указывающее, что все строковые свойства, переданные с вызовом, являются строками в Юникоде и имеют типы свойств ПТ_УНИКОДЕ.</span><span class="sxs-lookup"><span data-stu-id="a95b2-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="a95b2-110">В выходных данных этот флаг указывает на то, что все возвращенные значения свойств строки должны быть строками Юникода, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="a95b2-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="a95b2-111">Зависит ли значение флага для ввода или вывода от метода.</span><span class="sxs-lookup"><span data-stu-id="a95b2-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="a95b2-112">Разработчики таблиц, не поддерживающие Юникод и передаваемые флагом МАПИ_УНИКОДЕ, возвращают значение МАПИ_Е_БАД_ЧАР_ВИДС.</span><span class="sxs-lookup"><span data-stu-id="a95b2-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a95b2-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a95b2-113">See also</span></span>



[<span data-ttu-id="a95b2-114">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="a95b2-114">MAPI Tables</span></span>](mapi-tables.md)

