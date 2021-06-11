---
title: Использование макроса для обработки ошибок
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
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="1c523-103">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="1c523-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="1c523-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c523-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c523-105">Существует несколько макрос для упростить работу со значениями HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1c523-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="1c523-106">Существует два набора макрос, которые проверяют на неудачу или успех: HR_SUCCEEDED и HR_FAILED и FAILED и FAILED.</span><span class="sxs-lookup"><span data-stu-id="1c523-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="1c523-107">SUCCEEDED — это то же, HR_SUCCEEDED и FAILED — то же самое, что и HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="1c523-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="1c523-108">В этом случае используйте **макрос ResultFromScode,** чтобы задать переменную HRESULT соответствующему значению HRESULT для S_OK.</span><span class="sxs-lookup"><span data-stu-id="1c523-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="1c523-109">Обычно используемые макрос кратко описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1c523-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="1c523-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="1c523-110">**Macro**</span></span>|<span data-ttu-id="1c523-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c523-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c523-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1c523-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="1c523-113">Строит HRESULT из его компонентов.</span><span class="sxs-lookup"><span data-stu-id="1c523-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="1c523-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="1c523-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="1c523-115">Проверяет состояние HRESULT на успешность или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="1c523-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="1c523-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="1c523-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="1c523-117">Тесты HRESULT на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="1c523-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="1c523-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="1c523-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="1c523-119">Извлекает часть кода ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1c523-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="1c523-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="1c523-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="1c523-121">Извлекает объект из HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1c523-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="1c523-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="1c523-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="1c523-123">Извлекает немного серьезности из SEVERITY.</span><span class="sxs-lookup"><span data-stu-id="1c523-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="1c523-124">**SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="1c523-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="1c523-125">Проверяет состояние HRESULT на успешность или предупреждение.</span><span class="sxs-lookup"><span data-stu-id="1c523-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="1c523-126">**FAILED**</span><span class="sxs-lookup"><span data-stu-id="1c523-126">**FAILED**</span></span> <br/> |<span data-ttu-id="1c523-127">Тесты HRESULT на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="1c523-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

