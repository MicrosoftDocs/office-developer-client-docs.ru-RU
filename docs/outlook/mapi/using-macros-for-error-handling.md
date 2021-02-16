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
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="de057-103">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="de057-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="de057-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de057-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de057-105">Существует несколько макроса, которые упрощают работу со значениями HRESULT.</span><span class="sxs-lookup"><span data-stu-id="de057-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="de057-106">Существует два набора макросов, которые проверяют на сбой или успех: HR_SUCCEEDED и HR_FAILED и SUCCEEDED и FAILED.</span><span class="sxs-lookup"><span data-stu-id="de057-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="de057-107">SUCCEEDED это то же, HR_SUCCEEDED и FAILED то же, что и HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="de057-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="de057-108">В этом случае используйте макрос **ResultFromScode,** чтобы установить для переменной HRESULT соответствующее значение HRESULT для S_OK.</span><span class="sxs-lookup"><span data-stu-id="de057-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="de057-109">Часто используемые макрос кратко описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="de057-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="de057-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="de057-110">**Macro**</span></span>|<span data-ttu-id="de057-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de057-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de057-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de057-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="de057-113">Строит HRESULT из его компонентов.</span><span class="sxs-lookup"><span data-stu-id="de057-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="de057-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="de057-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="de057-115">Проверяет HRESULT на успешное состояние или условие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="de057-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="de057-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="de057-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="de057-117">Проверяет HRESULT на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="de057-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="de057-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="de057-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="de057-119">Извлекает часть кода ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="de057-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="de057-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="de057-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="de057-121">Извлекает объект из HRESULT.</span><span class="sxs-lookup"><span data-stu-id="de057-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="de057-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="de057-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="de057-123">Извлекает степень серьезности из степени серьезности.</span><span class="sxs-lookup"><span data-stu-id="de057-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="de057-124">**SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="de057-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="de057-125">Проверяет HRESULT на успешное состояние или условие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="de057-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="de057-126">**FAILED**</span><span class="sxs-lookup"><span data-stu-id="de057-126">**FAILED**</span></span> <br/> |<span data-ttu-id="de057-127">Проверяет HRESULT на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="de057-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

