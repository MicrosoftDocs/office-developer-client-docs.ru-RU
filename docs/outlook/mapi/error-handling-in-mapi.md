---
title: Обработка ошибок в MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287284"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="6ed9f-103">Обработка ошибок в MAPI</span><span class="sxs-lookup"><span data-stu-id="6ed9f-103">Error handling in MAPI</span></span>

<span data-ttu-id="6ed9f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ed9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ed9f-105">Значения успешности, предупреждения и ошибки возвращаются с помощью 32-битного числа, известного как десработка результатов, или HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="6ed9f-106">HRESULT на самом деле не является ни к чему; это просто 32-битное значение с несколькими полями, закодированные в значении.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="6ed9f-107">Нулевой результат указывает на успех, а ненулевой результат указывает на сбой.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="6ed9f-108">MAPI на 32-битных платформах работает исключительно со значениями HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="6ed9f-109">На следующем рисунке показан формат HRESULT для 32-битных платформ.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="6ed9f-110">**Формат HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6ed9f-110">**HRESULT format**</span></span>
  
<span data-ttu-id="6ed9f-111">![Формат HRESULT:](media/amapi_49.gif "HRESULT")</span><span class="sxs-lookup"><span data-stu-id="6ed9f-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="6ed9f-112">Бит высокого порядка в HRESULT указывает, означает ли возвращаемая величина успех или сбой.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="6ed9f-113">Если за установлено нулевое значение, значение указывает на успех.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="6ed9f-114">Если за установлено 1, это означает сбой.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="6ed9f-115">Биты R, C, N и r зарезервированы в HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="6ed9f-116">Поле объекта в обеих версиях указывает область ответственности за ошибку.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="6ed9f-117">Существует несколько средств, но большинство ошибок MAPI используют FACILITY_ITF для представления ошибок интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="6ed9f-118">Наиболее распространенные в настоящее время средства: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC и FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="6ed9f-119">При необходимости новые объекты корпорация Майкрософт выделяет их, так как они должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="6ed9f-120">В следующей таблице описываются различные поля объекта.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="6ed9f-121">Facility</span><span class="sxs-lookup"><span data-stu-id="6ed9f-121">Facility</span></span>|<span data-ttu-id="6ed9f-122">Описание</span><span class="sxs-lookup"><span data-stu-id="6ed9f-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ed9f-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="6ed9f-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="6ed9f-124">Для распространенных кодов состояния, таких как S_OK или E_OUTOF_MEMORY; значение — ноль.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="6ed9f-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="6ed9f-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="6ed9f-126">Для большинства кодов состояния, возвращаемого из методов интерфейса; значение определяется интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="6ed9f-127">То есть два значения HRESULT с точно таким же 32-битным значением, возвращаемого из двух разных интерфейсов, могут иметь разные значения.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="6ed9f-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="6ed9f-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="6ed9f-129">Для ошибок интерфейса [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) с поздней привязкой.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="6ed9f-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="6ed9f-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="6ed9f-131">Для кодов состояния, возвращаемого из удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="6ed9f-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="6ed9f-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="6ed9f-133">Для кодов состояния, возвращаемого из вызовов методов [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) или [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) связанных со структурированным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="6ed9f-134">Коды состояния со значениями кода (менее 16 битов) в диапазоне кодов ошибок Windows (то есть меньше 256) имеют то же значение, что и соответствующие ошибки Windows.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="6ed9f-135">Поле кода — это уникальное число, назначенное для представления ошибки или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

