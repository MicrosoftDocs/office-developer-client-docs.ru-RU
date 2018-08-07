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
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812576"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="2ca7e-103">Обработка ошибок с помощью макросов</span><span class="sxs-lookup"><span data-stu-id="2ca7e-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="2ca7e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ca7e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ca7e-105">Существует несколько макросов для облегчения работы со значениями HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="2ca7e-106">Существует два набора макросы, которые проверки успех или сбой: HR_SUCCEEDED и HR_FAILED и SUCCEEDED и FAILED.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="2ca7e-107">SUCCEEDED — то же, что HR_SUCCEEDED и FAILED совпадает с HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="2ca7e-108">В этом случае используйте макрос **ResultFromScode** для задания переменной HRESULT соответствующее значение HRESULT для значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="2ca7e-109">В следующей таблице кратко описаны часто используемые макросы.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="2ca7e-110">**Макрос**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-110">**Macro**</span></span>|<span data-ttu-id="2ca7e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ca7e-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="2ca7e-113">Создает HRESULT из ее компонентов.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="2ca7e-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="2ca7e-115">Проверяет HRESULT для успеха или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="2ca7e-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="2ca7e-117">Тесты со знаком для HRESULT ошибки.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="2ca7e-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="2ca7e-119">Извлекает часть кода ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="2ca7e-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="2ca7e-121">Извлекает средство из HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="2ca7e-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="2ca7e-123">Извлекает из СТЕПЕНИ разрядная уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="2ca7e-124">**ВЫПОЛНЕНО УСПЕШНО**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="2ca7e-125">Проверяет HRESULT для успеха или предупреждения.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="2ca7e-126">**НЕ УДАЛОСЬ**</span><span class="sxs-lookup"><span data-stu-id="2ca7e-126">**FAILED**</span></span> <br/> |<span data-ttu-id="2ca7e-127">Тесты со знаком для HRESULT ошибки.</span><span class="sxs-lookup"><span data-stu-id="2ca7e-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

