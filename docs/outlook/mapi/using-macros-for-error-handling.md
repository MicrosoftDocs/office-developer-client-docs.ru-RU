---
title: Использование макросов для обработки ошибок
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435567"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="83519-103">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="83519-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="83519-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83519-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83519-105">Существует несколько макросов, позволяющих упростить работу со значениями HRESULT.</span><span class="sxs-lookup"><span data-stu-id="83519-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="83519-106">Существует два набора макросов, которые проверяют сбой или успешное выполнение: ХР_СУКЦЕЕДЕД и ХР_ФАИЛЕД.</span><span class="sxs-lookup"><span data-stu-id="83519-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="83519-107">SUCCEEDED — то же, что и ХР_СУКЦЕЕДЕД, и сбой — то же самое, что и ХР_ФАИЛЕД.</span><span class="sxs-lookup"><span data-stu-id="83519-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="83519-108">В этом случае используйте макрос **ресултфромскоде** , чтобы присвоить переменной HRESULT СООТВЕТСТВУЮЩЕЕ значение HRESULT для S_OK.</span><span class="sxs-lookup"><span data-stu-id="83519-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="83519-109">Часто используемые макросы кратко описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="83519-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="83519-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="83519-110">**Macro**</span></span>|<span data-ttu-id="83519-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="83519-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83519-112">**МАКЕ_ХРЕСУЛТ**</span><span class="sxs-lookup"><span data-stu-id="83519-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="83519-113">Создает значение HRESULT из компонентов.</span><span class="sxs-lookup"><span data-stu-id="83519-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="83519-114">**ХР_СУКЦЕЕДЕД**</span><span class="sxs-lookup"><span data-stu-id="83519-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="83519-115">Проверяет значение HRESULT для условия "успешно" или "предупреждение".</span><span class="sxs-lookup"><span data-stu-id="83519-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="83519-116">**ХР_ФАИЛЕД**</span><span class="sxs-lookup"><span data-stu-id="83519-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="83519-117">Проверяет значение HRESULT для состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="83519-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="83519-118">**ХРЕСУЛТ_КОДЕ**</span><span class="sxs-lookup"><span data-stu-id="83519-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="83519-119">Извлекает часть кода ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="83519-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="83519-120">**ХРЕСУЛТ_ФАЦИЛИТИ**</span><span class="sxs-lookup"><span data-stu-id="83519-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="83519-121">Извлекает средство из HRESULT.</span><span class="sxs-lookup"><span data-stu-id="83519-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="83519-122">**ХРЕСУЛТ_СЕВЕРИТИ**</span><span class="sxs-lookup"><span data-stu-id="83519-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="83519-123">Извлекает бит серьезности из СЕРЬЕЗНОсти.</span><span class="sxs-lookup"><span data-stu-id="83519-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="83519-124">**ЗАКОНЧИЛ**</span><span class="sxs-lookup"><span data-stu-id="83519-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="83519-125">Проверяет значение HRESULT для условия "успешно" или "предупреждение".</span><span class="sxs-lookup"><span data-stu-id="83519-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="83519-126">**СБОЕВ**</span><span class="sxs-lookup"><span data-stu-id="83519-126">**FAILED**</span></span> <br/> |<span data-ttu-id="83519-127">Проверяет значение HRESULT для состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="83519-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

