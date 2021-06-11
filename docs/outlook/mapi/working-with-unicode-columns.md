---
title: Работа с столбцами Юникод
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408385"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="cc24a-103">Работа с столбцами Юникод</span><span class="sxs-lookup"><span data-stu-id="cc24a-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="cc24a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc24a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc24a-105">Строки символов в таблицах могут быть представлены с помощью стандартных 8-битных символов, которые являются свойствами типа PT_STRING8 или 16-битными символами Юникод, которые являются свойствами типа PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="cc24a-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="cc24a-106">Реализутели таблицы могут свободно выбирать, поддерживают ли их таблицы строки Юникод.</span><span class="sxs-lookup"><span data-stu-id="cc24a-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="cc24a-107">Поскольку Unicode добавляет значение как для клиентов, так и для поставщиков услуг, расширяя набор функций, рекомендуется поддерживать Юникод везде, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="cc24a-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="cc24a-108">Многие методы таблицы принимают флаг, который определяет, должны ли значения свойств строки быть Юникодом.</span><span class="sxs-lookup"><span data-stu-id="cc24a-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="cc24a-109">При вводе, указывая флаг MAPI_UNICODE, указывает на реализацию таблицы, что все значения свойств строки, переданные с вызовом, являются строками Юникод и имеют типы свойств PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="cc24a-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="cc24a-110">На выходе этот флаг указывает, что все возвращенные значения свойств строк должны быть строками Юникод, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="cc24a-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="cc24a-111">Значение флага для ввода или вывода зависит от метода.</span><span class="sxs-lookup"><span data-stu-id="cc24a-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="cc24a-112">Те, кто не поддерживает Юникод и передает флаг MAPI_UNICODE, возвращают MAPI_E_BAD_CHAR_WIDTH значение.</span><span class="sxs-lookup"><span data-stu-id="cc24a-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cc24a-113">См. также</span><span class="sxs-lookup"><span data-stu-id="cc24a-113">See also</span></span>



[<span data-ttu-id="cc24a-114">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="cc24a-114">MAPI Tables</span></span>](mapi-tables.md)

