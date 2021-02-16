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
# <a name="mapi-character-sets"></a><span data-ttu-id="a747a-103">Наборы символов MAPI</span><span class="sxs-lookup"><span data-stu-id="a747a-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="a747a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a747a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a747a-105">Клиентские приложения и поставщики служб, совместимые с MAPI, могут использовать символы ANSI (одинбайт) или Юникод (двойной).</span><span class="sxs-lookup"><span data-stu-id="a747a-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="a747a-106">Наборы символов OEM не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a747a-106">OEM character sets are not supported.</span></span> <span data-ttu-id="a747a-107">Строка OEM, переданная методу или функции MAPI, приведет к сбойу этого метода или функции.</span><span class="sxs-lookup"><span data-stu-id="a747a-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="a747a-108">Клиентские приложения, которые работают с именами файлов в наборе символов OEM, должны с осторожностью преобразовывать их в ANSI перед их передачей методу или функции MAPI.</span><span class="sxs-lookup"><span data-stu-id="a747a-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="a747a-109">Поддержка набора символов Юникод не является обязательной как для клиентов, так и для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="a747a-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="a747a-110">Все поставщики услуг должны написать свой код, чтобы они могли компилировать независимо от того, поддерживают ли они Юникод.</span><span class="sxs-lookup"><span data-stu-id="a747a-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="a747a-111">Клиенты компилировать условно, в зависимости от их уровня поддержки, а поставщики услуг нет.</span><span class="sxs-lookup"><span data-stu-id="a747a-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="a747a-112">При смене набора символов их не следует перекомпил использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="a747a-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="a747a-113">Ничего в коде поставщика услуг не должно быть условным.</span><span class="sxs-lookup"><span data-stu-id="a747a-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="a747a-114">Когда клиенты или поставщики услуг, которые поддерживают Юникод, делают вызов метода, который включает строки символов в качестве входных или выходных параметров, они устанавливают MAPI_UNICODE флаг.</span><span class="sxs-lookup"><span data-stu-id="a747a-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="a747a-115">Установка этого флага указывает реализации, что все входящие строки являются строками Юникода.</span><span class="sxs-lookup"><span data-stu-id="a747a-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="a747a-116">В выходных данных установка этого флага запрашивает, чтобы все строки, переданные из реализации, по возможности были строками Юникода.</span><span class="sxs-lookup"><span data-stu-id="a747a-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="a747a-117">Реализация методов, поддерживаюющих Юникод, будет соответствовать запросу; реализация методов, которые не обеспечивают поддержку Юникод, не будут соответствовать требованиям.</span><span class="sxs-lookup"><span data-stu-id="a747a-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="a747a-118">Строки свойств, не в формате Юникод, имеют тип PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="a747a-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="a747a-119">MAPI определяет **константы fMapiUnicode** в файле header MAPIDEFS. H для представления набора символов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a747a-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="a747a-120">Если клиент или поставщик услуг поддерживает Юникод, **для fMapiUnicode** устанавливается MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a747a-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="a747a-121">Клиенты и поставщики услуг, которые не поддерживают Юникод, задают **для fMapiUnicode** нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a747a-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="a747a-122">Поставщики услуг, которые не поддерживают Юникод, должны:</span><span class="sxs-lookup"><span data-stu-id="a747a-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="a747a-123">Отказаться от выполнения преобразований между наборами символов.</span><span class="sxs-lookup"><span data-stu-id="a747a-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="a747a-124">Никогда не передавать флаг MAPI_UNICODE в вызовах метода.</span><span class="sxs-lookup"><span data-stu-id="a747a-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="a747a-125">Возвращает MAPI_E_BAD_CHARWIDTH при MAPI_UNICODE флага.</span><span class="sxs-lookup"><span data-stu-id="a747a-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="a747a-126">Явно объявите свойства строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="a747a-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="a747a-127">Поставщики услуг также могут возвращать MAPI_E_BAD_CHARWIDTH, если они поддерживают только Юникод, а клиенты не передают MAPI_UNICODE флаг.</span><span class="sxs-lookup"><span data-stu-id="a747a-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="a747a-128">Текущая версия MAPI поддерживает Юникод в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="a747a-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="a747a-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="a747a-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="a747a-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="a747a-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="a747a-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="a747a-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="a747a-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="a747a-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="a747a-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) ( только реализация **IAddrBook)**</span><span class="sxs-lookup"><span data-stu-id="a747a-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="a747a-134">Для этих методов вызыватели могут ожидать, что любые возвращенные строки будут строками Юникода.</span><span class="sxs-lookup"><span data-stu-id="a747a-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="a747a-135">Строки символов, возвращенные из реализации MAPI любого другого метода, будут строками символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="a747a-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

