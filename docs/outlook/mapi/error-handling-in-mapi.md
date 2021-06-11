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
# <a name="error-handling-in-mapi"></a><span data-ttu-id="c3df3-103">Обработка ошибок в MAPI</span><span class="sxs-lookup"><span data-stu-id="c3df3-103">Error handling in MAPI</span></span>

<span data-ttu-id="c3df3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3df3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3df3-105">Значения успешности, предупреждения и ошибок возвращаются с помощью 32-битного номера, известного как обработка результатов, или HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c3df3-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="c3df3-106">HRESULT на самом деле не является ручкой для чего-либо; это всего лишь 32-битное значение с несколькими полями, закодированные в значении.</span><span class="sxs-lookup"><span data-stu-id="c3df3-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="c3df3-107">Нулевой результат указывает на успех, а незерный результат указывает на сбой.</span><span class="sxs-lookup"><span data-stu-id="c3df3-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="c3df3-108">MAPI на 32-битных платформах работает исключительно со значениями HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c3df3-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="c3df3-109">На следующем рисунке показан формат HRESULT для 32-битных платформ.</span><span class="sxs-lookup"><span data-stu-id="c3df3-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="c3df3-110">**Формат HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c3df3-110">**HRESULT format**</span></span>
  
<span data-ttu-id="c3df3-111">![ФОРМАТ HRESULT формат](media/amapi_49.gif "HRESULT")</span><span class="sxs-lookup"><span data-stu-id="c3df3-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="c3df3-112">Бит высокого порядка в HRESULT указывает, является ли возвращаемая величина успешной или неудачной.</span><span class="sxs-lookup"><span data-stu-id="c3df3-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="c3df3-113">Если значение установлено до нуля, значение указывает на успех.</span><span class="sxs-lookup"><span data-stu-id="c3df3-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="c3df3-114">Если установлено 1, это указывает на сбой.</span><span class="sxs-lookup"><span data-stu-id="c3df3-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="c3df3-115">Биты R, C, N и r зарезервированы в HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c3df3-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="c3df3-116">Поле объекта в обеих версиях указывает область ответственности за ошибку.</span><span class="sxs-lookup"><span data-stu-id="c3df3-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="c3df3-117">Существует несколько объектов, но подавляющее большинство ошибок MAPI FACILITY_ITF для представления ошибок интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c3df3-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="c3df3-118">Наиболее распространенными средствами, используемыми в настоящее время, являются: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC и FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="c3df3-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="c3df3-119">Если необходимы новые возможности, Корпорация Майкрософт выделяет их, так как они должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="c3df3-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="c3df3-120">В следующей таблице описываются различные поля объекта.</span><span class="sxs-lookup"><span data-stu-id="c3df3-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="c3df3-121">Facility</span><span class="sxs-lookup"><span data-stu-id="c3df3-121">Facility</span></span>|<span data-ttu-id="c3df3-122">Описание</span><span class="sxs-lookup"><span data-stu-id="c3df3-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="c3df3-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="c3df3-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="c3df3-124">Для широко применимых общих кодов состояния, таких как S_OK или E_OUTOF_MEMORY; значение нулевое.</span><span class="sxs-lookup"><span data-stu-id="c3df3-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="c3df3-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="c3df3-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="c3df3-126">Для большинства кодов состояния, возвращаемого из методов интерфейса; значение определяется интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="c3df3-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="c3df3-127">То есть два значения HRESULT с одинаковым 32-битным значением, возвращаемого из двух различных интерфейсов, могут иметь разные значения.</span><span class="sxs-lookup"><span data-stu-id="c3df3-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="c3df3-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="c3df3-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="c3df3-129">Для поздних [ошибок интерфейса IDispatch.](https://msdn.microsoft.com/library/ms221608.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3df3-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="c3df3-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="c3df3-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="c3df3-131">Для кодов состояния, возвращаемого из удаленных вызовов процедуры.</span><span class="sxs-lookup"><span data-stu-id="c3df3-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="c3df3-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="c3df3-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="c3df3-133">Для кодов состояния, возвращающихся из [вызовов методов IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) или [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) связанных со структурированным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="c3df3-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="c3df3-134">Коды состояния со значениями кода (менее 16 бит) в диапазоне Windows кодов ошибок (то есть менее 256) имеют то же значение, что и соответствующие Windows ошибки.</span><span class="sxs-lookup"><span data-stu-id="c3df3-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="c3df3-135">Поле кода — это уникальный номер, который назначен для представления ошибки или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="c3df3-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

