---
title: Соглашение об именовании возвращаемых значений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279827"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="790cc-103">Соглашение об именовании возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="790cc-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="790cc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="790cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="790cc-105">МАПИКОДЕ. H файл заголовка содержит множество значений, которые клиент или поставщик услуг может возвращать из реализации метода интерфейса или могут отображаться при возврате из вызова.</span><span class="sxs-lookup"><span data-stu-id="790cc-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="790cc-106">Коды для представления предупреждений и условий сбоя следуют по другому соглашению об именовании, которое начинается с префикса MAPI, знака подчеркивания и числа W или E, чтобы указать тип кода.</span><span class="sxs-lookup"><span data-stu-id="790cc-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="790cc-107">Остальная часть кода — это короткая строка символов, описывающая условие.</span><span class="sxs-lookup"><span data-stu-id="790cc-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="790cc-108">Каждое слово в строке отделяется подчеркиванием.</span><span class="sxs-lookup"><span data-stu-id="790cc-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="790cc-109">Например, значение ошибки МАПИ_Е_ТУ_КОМПЛЕКС указывает на то, что во время вызова не удается обработать все запросы, которые были запрошены.</span><span class="sxs-lookup"><span data-stu-id="790cc-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="790cc-110">Значение предупреждения МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН указывает, что вызов выполнен успешно, но возникли проблемы.</span><span class="sxs-lookup"><span data-stu-id="790cc-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="790cc-111">Успешно выполнена только часть операции.</span><span class="sxs-lookup"><span data-stu-id="790cc-111">Only part of the operation was completed successfully.</span></span>
  

