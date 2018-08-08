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
ms.openlocfilehash: 6f0ebd2112b65140a106a1376896f6de9c00da1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808390"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="6fd9b-103">Обработка ошибок в MAPI</span><span class="sxs-lookup"><span data-stu-id="6fd9b-103">Error handling in MAPI</span></span>

<span data-ttu-id="6fd9b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6fd9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6fd9b-105">Успех, предупреждения и ошибки значения возвращаются с помощью 32-разрядное число, в результате известные дескриптор или HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="6fd9b-106">HRESULT самом деле не маркер на что-либо; Это просто значение 32-разрядная версия с несколько полей в значения кодировке.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="6fd9b-107">Нулевой результат означает успешное выполнение и отличное от нуля результат указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="6fd9b-108">MAPI на 32-разрядных платформах работает только с значения HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="6fd9b-109">На следующем рисунке показана формат HRESULT для 32-разрядных платформ.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="6fd9b-110">**Формат HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6fd9b-110">**HRESULT format**</span></span>
  
<span data-ttu-id="6fd9b-111">![Формат HRESULT] (media/amapi_49.gif "Формат HRESULT")</span><span class="sxs-lookup"><span data-stu-id="6fd9b-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="6fd9b-112">Старшего бита в значение HRESULT указывает тип возвращаемого значения: успешное или неудачное.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="6fd9b-113">Если значение 0, значение указывает на успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="6fd9b-114">Если задано значение 1, это означает сбой.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="6fd9b-115">R, C, N и r бит зарезервированные в значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="6fd9b-116">Поле оборудование в обеих версиях указывает области ответственности для ошибки.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="6fd9b-117">Существует несколько средств, однако большинство ошибок MAPI использовать FACILITY_ITF для представления ошибки интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="6fd9b-118">Наиболее распространенные производственные объекты, используемые в настоящее время являются: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC и FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="6fd9b-119">При необходимости новые функции Microsoft выделяет их, так как они должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="6fd9b-120">В следующей таблице описаны различные поля оборудование.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="6fd9b-121">Оборудование</span><span class="sxs-lookup"><span data-stu-id="6fd9b-121">Facility</span></span>|<span data-ttu-id="6fd9b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="6fd9b-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="6fd9b-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="6fd9b-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="6fd9b-124">Для широко применяемые основные коды состояния, таких как значение S_OK или E_OUTOF_MEMORY; значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="6fd9b-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="6fd9b-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="6fd9b-126">Для большинства коды состояния, возвращаемые из методов интерфейса; значение определяется с помощью интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="6fd9b-127">То есть два значения HRESULT точно совпадает с 32-разрядная версия возвращаются из двух разных интерфейсов может иметь различные значения.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="6fd9b-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="6fd9b-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="6fd9b-129">Позднего связывания [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) интерфейса ошибки.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-129">For late binding [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="6fd9b-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="6fd9b-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="6fd9b-131">Для коды состояния, возвращаемые из удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="6fd9b-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="6fd9b-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="6fd9b-133">Для коды состояния, возвращаемые [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) или [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) вызовы методов, относящиеся к структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-133">For status codes returned from [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) or [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="6fd9b-134">Коды состояния кода (меньше 16 бит) значения в диапазоне Windows коды ошибок (то есть, не превышает 256) значение соответствующего ошибки Windows.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="6fd9b-135">В поле Код — уникальный номер, назначенный для представления сообщение об ошибке или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="6fd9b-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

