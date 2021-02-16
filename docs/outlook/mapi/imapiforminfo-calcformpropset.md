---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0b62c21348da71c1ee863f70d6e6a549a5d10003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438073"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="0d5dd-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="0d5dd-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="0d5dd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d5dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d5dd-105">Возвращает указатель на полный набор свойств, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="0d5dd-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="0d5dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d5dd-106">Parameters</span></span>

 <span data-ttu-id="0d5dd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d5dd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0d5dd-108">[in] Битоваяmas флагов, которая управляет типом возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="0d5dd-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="0d5dd-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0d5dd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0d5dd-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d5dd-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0d5dd-111">Возвращенные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="0d5dd-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="0d5dd-112">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0d5dd-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0d5dd-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="0d5dd-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="0d5dd-114">[out] Указатель на указатель на возвращенную [структуру SMAPIFormPropArray.](smapiformproparray.md)</span><span class="sxs-lookup"><span data-stu-id="0d5dd-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d5dd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d5dd-115">Return value</span></span>

<span data-ttu-id="0d5dd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d5dd-116">S_OK</span></span> 
  
> <span data-ttu-id="0d5dd-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0d5dd-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0d5dd-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0d5dd-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0d5dd-119">Либо флаг MAPI_UNICODE установлен и реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="0d5dd-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0d5dd-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0d5dd-120">MFCMAPI reference</span></span>

<span data-ttu-id="0d5dd-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0d5dd-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0d5dd-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0d5dd-122">**File**</span></span>|<span data-ttu-id="0d5dd-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0d5dd-123">**Function**</span></span>|<span data-ttu-id="0d5dd-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0d5dd-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d5dd-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="0d5dd-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="0d5dd-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="0d5dd-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="0d5dd-127">MFCMAPI использует метод **IMAPIFormInfo::CalcFormPropSet** при записи выходных данных отлаки для информационных объектов формы.</span><span class="sxs-lookup"><span data-stu-id="0d5dd-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d5dd-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0d5dd-128">See also</span></span>



[<span data-ttu-id="0d5dd-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="0d5dd-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="0d5dd-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0d5dd-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="0d5dd-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0d5dd-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

