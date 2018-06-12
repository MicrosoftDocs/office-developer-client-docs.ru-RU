---
title: Работа со столбцами Юникод
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 9f1fd2d4e4bfdc9ccbbb771fedf1141769c8c8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812598"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="c0bc2-103">Работа со столбцами Юникод</span><span class="sxs-lookup"><span data-stu-id="c0bc2-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="c0bc2-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0bc2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0bc2-105">С помощью стандартных 8-разрядных символов, которые тип свойства PT_STRING8, или знаки Юникода 16-разрядной, которые являются тип свойства PT_UNICODE может быть представлена строк в таблицах.</span><span class="sxs-lookup"><span data-stu-id="c0bc2-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="c0bc2-106">В таблице специалистов по внедрению могут выбирать, поддерживает ли их таблицы строк в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="c0bc2-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="c0bc2-107">Так как Юникод добавляет значение для клиентов и поставщиков услуг, расширяя набор функций, рекомендуется поддержки Юникод, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="c0bc2-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="c0bc2-108">Множество методов в таблице принимать флаг, который определяет ли строковые значения свойства должны быть Юникод.</span><span class="sxs-lookup"><span data-stu-id="c0bc2-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="c0bc2-109">На входе задание флаг MAPI_UNICODE указывает для разработчика в таблице, что все строковые значения свойства, переданными вызова строки Юникод и имеют типы свойств из PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c0bc2-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="c0bc2-110">В выходных данных этот флаг указывает, что все значения свойств Возвращенная строка должно быть строки Юникод, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="c0bc2-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="c0bc2-111">Является ли флаг имеет значение для ввода или вывода, зависит от метода.</span><span class="sxs-lookup"><span data-stu-id="c0bc2-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="c0bc2-112">В таблице специалистов по внедрению, которые не поддерживают Юникод и передаются флаг MAPI_UNICODE возвращать значение MAPI_E_BAD_CHAR_WIDTH.</span><span class="sxs-lookup"><span data-stu-id="c0bc2-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0bc2-113">См. также</span><span class="sxs-lookup"><span data-stu-id="c0bc2-113">See also</span></span>



[<span data-ttu-id="c0bc2-114">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="c0bc2-114">MAPI Tables</span></span>](mapi-tables.md)

