---
title: Return Value Naming Convention
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423617"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="316c6-103">Return Value Naming Convention</span><span class="sxs-lookup"><span data-stu-id="316c6-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="316c6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="316c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="316c6-105">The MAPICODE. Файл загона H содержит множество значений, которые клиент или поставщик услуг может вернуться из реализации метода интерфейса или увидеть возвращенные из вызова.</span><span class="sxs-lookup"><span data-stu-id="316c6-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="316c6-106">Коды, которые представляют условия предупреждения и сбоя, следуют другой конвенции именования, которая начинается с префикса MAPI, подчеркивания и W или E, чтобы указать тип кода.</span><span class="sxs-lookup"><span data-stu-id="316c6-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="316c6-107">Остальная часть кода — это короткая строка символов для описания условия.</span><span class="sxs-lookup"><span data-stu-id="316c6-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="316c6-108">Каждое слово в строке разделено подчеркиваемой строкой.</span><span class="sxs-lookup"><span data-stu-id="316c6-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="316c6-109">Например, значение ошибки MAPI_E_TOO_COMPLEX, что реализация не может обрабатывать все, что запрашивалось в вызове.</span><span class="sxs-lookup"><span data-stu-id="316c6-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="316c6-110">Значение предупреждения MAPI_W_PARTIAL_COMPLETION, что вызов удался, но возникли проблемы.</span><span class="sxs-lookup"><span data-stu-id="316c6-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="316c6-111">Успешно выполнена только часть операции.</span><span class="sxs-lookup"><span data-stu-id="316c6-111">Only part of the operation was completed successfully.</span></span>
  

