---
title: Работа со столбцами Юникода
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
# <a name="working-with-unicode-columns"></a><span data-ttu-id="4f4d5-103">Работа со столбцами Юникода</span><span class="sxs-lookup"><span data-stu-id="4f4d5-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="4f4d5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f4d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f4d5-105">Строки символов в таблицах могут быть представлены с помощью стандартных 8-битных символов, которые являются типом свойства PT_STRING8, или 16-битных символов Юникода, которые являются типом свойства PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="4f4d5-106">Те, кто реализует таблицы, могут самостоятельно выбирать, поддерживают ли их таблицы строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="4f4d5-107">Так как Юникод добавляет значение как для клиентов, так и для поставщиков услуг, расширяя набор функций, рекомендуется поддерживать Юникод везде, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="4f4d5-108">Многие методы таблиц принимают флаг, который определяет, должны ли значения строки свойства быть Юникодом.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="4f4d5-109">При вводе флаг MAPI_UNICODE указывает средству реализации таблицы, что все значения строки свойств, переданные вызовом, являются строками Юникода и имеют типы свойств PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="4f4d5-110">В выходных данных этот флаг указывает, что все возвращенные значения строки свойства должны быть строками Юникода, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="4f4d5-111">Значение флага для ввода или вывода зависит от метода.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="4f4d5-112">Те, кто реализует таблицы, которые не поддерживают Юникод и передают флаг MAPI_UNICODE, возвращают MAPI_E_BAD_CHAR_WIDTH значение.</span><span class="sxs-lookup"><span data-stu-id="4f4d5-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f4d5-113">См. также</span><span class="sxs-lookup"><span data-stu-id="4f4d5-113">See also</span></span>



[<span data-ttu-id="4f4d5-114">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="4f4d5-114">MAPI Tables</span></span>](mapi-tables.md)

