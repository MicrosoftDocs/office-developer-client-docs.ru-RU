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
ms.openlocfilehash: 3f94823eb3f90ff9ac0f472a2de64e1904920d9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809714"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="bf141-103">Наборы символов MAPI</span><span class="sxs-lookup"><span data-stu-id="bf141-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="bf141-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf141-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf141-105">MAPI-совместимое клиентских приложений и поставщиков услуг можно использовать символы ANSI (один байт) или знаки Юникода (два байта).</span><span class="sxs-lookup"><span data-stu-id="bf141-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="bf141-106">Наборы символов ПВТ не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="bf141-106">OEM character sets are not supported.</span></span> <span data-ttu-id="bf141-107">Строку OEM, переданной в метод MAPI или в функции, метода или функции могут быть.</span><span class="sxs-lookup"><span data-stu-id="bf141-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="bf141-108">Клиентские приложения, которые работают с именами файлов в набор символов OEM необходимо следить за тем преобразовать их в формате ANSI перед передачей их в метод MAPI или функции.</span><span class="sxs-lookup"><span data-stu-id="bf141-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="bf141-109">Поддержка Юникода набор знаков является необязательным, как для клиентов и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="bf141-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="bf141-110">Все поставщики услуг следует писать код, чтобы их можно компилировать вне зависимости от того, является ли они поддерживают Юникод.</span><span class="sxs-lookup"><span data-stu-id="bf141-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="bf141-111">Клиенты компиляции, в зависимости от их уровень поддержки, но не поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="bf141-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="bf141-112">Они не должны быть перекомпилированы при изменения набор символов.</span><span class="sxs-lookup"><span data-stu-id="bf141-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="bf141-113">Значение Nothing в коде поставщика службы должны быть условного.</span><span class="sxs-lookup"><span data-stu-id="bf141-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="bf141-114">Если клиенты или поставщиков услуг, которые поддерживают Юникод сделать вызов метода, который включает в себя строки символ в качестве входных и выходных параметров, они параметр флаг MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bf141-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="bf141-115">Установка этот флаг указывает реализации, что все входящие строки являются строк в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="bf141-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="bf141-116">На выходных данных установка этот флаг запросов, всех строк, передаваемых резервного от реализации должны быть строк в кодировке Юникод, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="bf141-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="bf141-117">Метод специалистов по внедрению, которые поддерживают Юникод будет соответствовать запроса; не будет соответствовать специалистов по внедрению метода, которые не поддерживают Юникод.</span><span class="sxs-lookup"><span data-stu-id="bf141-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="bf141-118">Строковые свойства, которые не являются в формате Юникод, типа PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="bf141-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="bf141-119">MAPI определяет константу **fMapiUnicode** в файле заголовка MAPIDEFS. H для представления набор знаков по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bf141-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="bf141-120">Если клиент или служба поставщик поддерживает Юникод, **fMapiUnicode** имеет значение MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bf141-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="bf141-121">Клиенты и поставщики услуг, которые не поддерживают Юникод задайте **fMapiUnicode** присваивается значение 0.</span><span class="sxs-lookup"><span data-stu-id="bf141-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="bf141-122">Поставщики услуг, которые не поддерживают Юникод выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bf141-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="bf141-123">Отказ от выполнения преобразований между наборы символов.</span><span class="sxs-lookup"><span data-stu-id="bf141-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="bf141-124">Никогда не передайте флаг MAPI_UNICODE вызовы методов.</span><span class="sxs-lookup"><span data-stu-id="bf141-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="bf141-125">Возвращает MAPI_E_BAD_CHARWIDTH, когда флаг MAPI_UNICODE передается в.</span><span class="sxs-lookup"><span data-stu-id="bf141-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="bf141-126">Явным образом объявите свойства строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="bf141-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="bf141-127">Поставщиков услуг может также возвращать MAPI_E_BAD_CHARWIDTH, когда они поддерживают только Юникод и клиенты не передавайте флаг MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bf141-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="bf141-128">Текущая версия MAPI поддерживает Юникод в следующих методов:</span><span class="sxs-lookup"><span data-stu-id="bf141-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="bf141-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="bf141-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="bf141-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="bf141-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="bf141-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="bf141-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="bf141-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="bf141-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="bf141-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Только для реализации**IAddrBook** )</span><span class="sxs-lookup"><span data-stu-id="bf141-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="bf141-134">Для этих методов абонентов может предполагать любые возвращенные строки строки Юникод.</span><span class="sxs-lookup"><span data-stu-id="bf141-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="bf141-135">Строк, возвращенных MAPI реализации любой другой метод будет строк символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="bf141-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

