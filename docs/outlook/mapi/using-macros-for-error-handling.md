---
title: Обработка ошибок с помощью макросов
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567127"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="e8d24-103">Обработка ошибок с помощью макросов</span><span class="sxs-lookup"><span data-stu-id="e8d24-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="e8d24-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8d24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8d24-105">Существует несколько макросов для облегчения работы со значениями HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e8d24-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="e8d24-106">Существует два набора макросы, которые проверки успех или сбой: HR_SUCCEEDED и HR_FAILED и SUCCEEDED и FAILED.</span><span class="sxs-lookup"><span data-stu-id="e8d24-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="e8d24-107">SUCCEEDED — то же, что HR_SUCCEEDED и FAILED совпадает с HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="e8d24-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="e8d24-108">В этом случае используйте макрос **ResultFromScode** для задания переменной HRESULT соответствующее значение HRESULT для значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="e8d24-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="e8d24-109">В следующей таблице кратко описаны часто используемые макросы.</span><span class="sxs-lookup"><span data-stu-id="e8d24-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="e8d24-110">**Макрос**</span><span class="sxs-lookup"><span data-stu-id="e8d24-110">**Macro**</span></span>|<span data-ttu-id="e8d24-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8d24-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8d24-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e8d24-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="e8d24-113">Создает HRESULT из ее компонентов.</span><span class="sxs-lookup"><span data-stu-id="e8d24-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="e8d24-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="e8d24-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="e8d24-115">Проверяет HRESULT для успеха или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="e8d24-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="e8d24-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="e8d24-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="e8d24-117">Тесты со знаком для HRESULT ошибки.</span><span class="sxs-lookup"><span data-stu-id="e8d24-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="e8d24-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="e8d24-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="e8d24-119">Извлекает часть кода ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e8d24-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="e8d24-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="e8d24-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="e8d24-121">Извлекает средство из HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e8d24-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="e8d24-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="e8d24-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="e8d24-123">Извлекает из СТЕПЕНИ разрядная уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="e8d24-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="e8d24-124">**ВЫПОЛНЕНО УСПЕШНО**</span><span class="sxs-lookup"><span data-stu-id="e8d24-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="e8d24-125">Проверяет HRESULT для успеха или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="e8d24-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="e8d24-126">**НЕ УДАЛОСЬ**</span><span class="sxs-lookup"><span data-stu-id="e8d24-126">**FAILED**</span></span> <br/> |<span data-ttu-id="e8d24-127">Тесты со знаком для HRESULT ошибки.</span><span class="sxs-lookup"><span data-stu-id="e8d24-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

