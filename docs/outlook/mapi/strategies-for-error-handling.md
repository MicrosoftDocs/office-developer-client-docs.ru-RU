---
title: Стратегии обработки ошибок
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812391"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="18075-103">Стратегии обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="18075-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="18075-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18075-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18075-105">Как виртуальные методы интерфейса не поддерживается знаете, как вызывающего абонента, полный набор значений, которые можно получить из любого один звонок.</span><span class="sxs-lookup"><span data-stu-id="18075-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="18075-106">Реализация метода может вернуть пять значения; другое может возвращать восемь.</span><span class="sxs-lookup"><span data-stu-id="18075-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="18075-107">Список записей ссылку в документации по MAPI несколько значений, которые могут быть возвращены для каждого метода. Это значения, которые можно искать и обработать, так как они особое значение вашего клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="18075-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="18075-108">Другие значения могут быть возвращены, но поскольку они не удобной для восприятия, специальные код для обработки тех не требуется.</span><span class="sxs-lookup"><span data-stu-id="18075-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="18075-109">Простой поиск успешное или неудачное достаточное количество.</span><span class="sxs-lookup"><span data-stu-id="18075-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="18075-110">Некоторые из методов интерфейса возврата предупреждения.</span><span class="sxs-lookup"><span data-stu-id="18075-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="18075-111">Если метод, который вызывает вашего клиента или поставщика можно вернуть предупреждения, используйте макрос **HR_FAILED** для тестирования возвращаемого значения, а не выполняется проверка для нуля или отличное от нуля.</span><span class="sxs-lookup"><span data-stu-id="18075-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="18075-112">Предупреждения, хотя ненулевое значение, отличаются от коды ошибок в том, что у них нет высокой бит.</span><span class="sxs-lookup"><span data-stu-id="18075-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="18075-113">Если ваш поставщик клиента или службы не использует макрос, скорее всего, что предупреждение может означает сбой.</span><span class="sxs-lookup"><span data-stu-id="18075-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="18075-114">Хотя большинство методов интерфейса и функции, возвращаемые значения HRESULT, некоторые функции возвращают неподписанных длинные значения.</span><span class="sxs-lookup"><span data-stu-id="18075-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="18075-115">Кроме того некоторые методы, используемые в среде MAPI поступают из COM и возвращают COM ошибочные значения, а не значения ошибка MAPI.</span><span class="sxs-lookup"><span data-stu-id="18075-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="18075-116">При выполнении вызовов учитывайте следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="18075-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="18075-117">Никогда не зависеть от или возвращаемого значения из **IUnknown::AddRef** или **функции IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="18075-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="18075-118">Эти значения будут возвращены только в целях диагностики.</span><span class="sxs-lookup"><span data-stu-id="18075-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="18075-119">**IUnknown::QueryInterface** всегда возвращает универсальный ошибки COM, где — это средство FACILITY_NULL или FACILITY_RPC, а не ошибки MAPI.</span><span class="sxs-lookup"><span data-stu-id="18075-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="18075-120">Все другие методы интерфейса возвращает ошибки интерфейса MAPI с помощью средства FACILITY_ITF или FACILITY_RPC или FACILITY_NULL ошибки.</span><span class="sxs-lookup"><span data-stu-id="18075-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="18075-121">При вызове не поддерживается методу MAPI могут быть возвращены одним из четырех возможных ошибок:</span><span class="sxs-lookup"><span data-stu-id="18075-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="18075-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="18075-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="18075-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="18075-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="18075-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="18075-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="18075-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="18075-125">MAPI_E_VERSION.</span></span> 
  

