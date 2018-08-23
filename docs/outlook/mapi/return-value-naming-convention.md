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
ms.openlocfilehash: 4d7a95e4681370e1aaf4f8b4c4b7ca0814b3aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581848"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="02dd2-103">Соглашение об именовании возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="02dd2-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="02dd2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02dd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02dd2-105">MAPICODE. Файл заголовка содержит множество значений, что клиента или поставщика, может возвращать из реализацию метода интерфейса или может видеть возвращенных из звонка.</span><span class="sxs-lookup"><span data-stu-id="02dd2-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="02dd2-106">Коды для представления условия предупреждения и ошибки выполните различных соглашение об именовании, начинающийся с префикса MAPI, знака подчеркивания и W или E, чтобы указать тип кода.</span><span class="sxs-lookup"><span data-stu-id="02dd2-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="02dd2-107">Оставшуюся часть кода является строкой краткое символов для описания условие.</span><span class="sxs-lookup"><span data-stu-id="02dd2-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="02dd2-108">Каждого слова в строке, разделенных символом подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="02dd2-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="02dd2-109">Например значение ошибки MAPI_E_TOO_COMPLEX указывает, что реализации может не обрабатывать все, что был запрошен в вызове.</span><span class="sxs-lookup"><span data-stu-id="02dd2-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="02dd2-110">Значение MAPI_W_PARTIAL_COMPLETION указывает, что вызов завершился успешно, но, что возникли проблемы.</span><span class="sxs-lookup"><span data-stu-id="02dd2-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="02dd2-111">Часть операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="02dd2-111">Only part of the operation was completed successfully.</span></span>
  

