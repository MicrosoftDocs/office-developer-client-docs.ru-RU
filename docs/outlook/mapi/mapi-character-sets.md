---
title: Наборы символов MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417555"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="c0e90-103">Наборы символов MAPI</span><span class="sxs-lookup"><span data-stu-id="c0e90-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="c0e90-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0e90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0e90-105">Клиентские приложения и поставщики услуг, совместимые с MAPI, могут использовать символы ANSI (однобайтные) или символы Юникод (двойной byte).</span><span class="sxs-lookup"><span data-stu-id="c0e90-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="c0e90-106">Наборы символов OEM не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c0e90-106">OEM character sets are not supported.</span></span> <span data-ttu-id="c0e90-107">Строка OEM, переданная методу или функции MAPI, приведет к сбой этого метода или функции.</span><span class="sxs-lookup"><span data-stu-id="c0e90-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="c0e90-108">Клиентские приложения, которые работают с именами файлов в наборе символов OEM, должны быть осторожны, чтобы преобразовать их в ANSI перед передачей их в метод MAPI или функцию.</span><span class="sxs-lookup"><span data-stu-id="c0e90-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="c0e90-109">Поддержка набора символов Unicode необязательна как для клиентов, так и для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="c0e90-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="c0e90-110">Все поставщики услуг должны написать свой код, чтобы они могли компилировать независимо от того, поддерживают ли они Юникод.</span><span class="sxs-lookup"><span data-stu-id="c0e90-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="c0e90-111">Клиенты компиляторяются условно, в зависимости от уровня поддержки, но поставщики услуг этого не делают.</span><span class="sxs-lookup"><span data-stu-id="c0e90-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="c0e90-112">При изменениях набора символов их не следует перекомпактовки.</span><span class="sxs-lookup"><span data-stu-id="c0e90-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="c0e90-113">Ничто в коде поставщика услуг не должно быть условным.</span><span class="sxs-lookup"><span data-stu-id="c0e90-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="c0e90-114">Когда клиенты или поставщики услуг, поддерживают Юникод, делают вызов метода, который включает строки символов в качестве параметров ввода или вывода, они задают MAPI_UNICODE флаг.</span><span class="sxs-lookup"><span data-stu-id="c0e90-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="c0e90-115">Установка этого флага указывает на реализацию, что все входящие строки являются строками Unicode.</span><span class="sxs-lookup"><span data-stu-id="c0e90-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="c0e90-116">На выходе задав этот флаг, все строки, переданные из реализации, должны быть строками Юникод, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="c0e90-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="c0e90-117">Реализутели метода, поддерживают Юникод, будут соответствовать запросу; Не соответствуют требованиям реализации методов, которые не предоставляют поддержку Юникод.</span><span class="sxs-lookup"><span data-stu-id="c0e90-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="c0e90-118">Свойства строк, не в формате Unicode, имеют тип PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="c0e90-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="c0e90-119">MAPI определяет констант **fMapiUnicode** в файле MAPIDEFS заголовки. H для представления набора символов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0e90-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="c0e90-120">Если клиент или поставщик услуг поддерживает Юникод, **fMapiUnicode** задает MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c0e90-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="c0e90-121">Клиенты и поставщики услуг, которые не поддерживают набор Юникод **fMapiUnicode** до нуля.</span><span class="sxs-lookup"><span data-stu-id="c0e90-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="c0e90-122">Поставщики услуг, которые не поддерживают Unicode, должны:</span><span class="sxs-lookup"><span data-stu-id="c0e90-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="c0e90-123">Отказ от выполнения преобразований между наборами символов.</span><span class="sxs-lookup"><span data-stu-id="c0e90-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="c0e90-124">Никогда не передай флаг MAPI_UNICODE при вызове метода.</span><span class="sxs-lookup"><span data-stu-id="c0e90-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="c0e90-125">Возврат MAPI_E_BAD_CHARWIDTH при MAPI_UNICODE флага.</span><span class="sxs-lookup"><span data-stu-id="c0e90-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="c0e90-126">Объявите свойства строки ANSI явно.</span><span class="sxs-lookup"><span data-stu-id="c0e90-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="c0e90-127">Поставщики услуг также могут возвращать MAPI_E_BAD_CHARWIDTH, когда поддерживают только Юникод, а клиенты не передают MAPI_UNICODE флаг.</span><span class="sxs-lookup"><span data-stu-id="c0e90-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="c0e90-128">Текущая версия MAPI поддерживает Юникод в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="c0e90-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="c0e90-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="c0e90-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="c0e90-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="c0e90-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="c0e90-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="c0e90-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="c0e90-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="c0e90-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="c0e90-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) **(только реализация IAddrBook)**</span><span class="sxs-lookup"><span data-stu-id="c0e90-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="c0e90-134">Для этих методов звонители могут ожидать, что любые возвращенные строки будут строками Юникод.</span><span class="sxs-lookup"><span data-stu-id="c0e90-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="c0e90-135">Строки символов, возвращенные из реализации MAPI любого другого метода, будут строками символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="c0e90-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

