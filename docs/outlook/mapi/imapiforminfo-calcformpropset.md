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
ms.openlocfilehash: 7d0c044caf430c944d8912d050e4dbaba659c8b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582499"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="91f4f-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="91f4f-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="91f4f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91f4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91f4f-105">Возвращает указатель на полный набор свойств, используемых в форме.</span><span class="sxs-lookup"><span data-stu-id="91f4f-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="91f4f-106">���������</span><span class="sxs-lookup"><span data-stu-id="91f4f-106">Parameters</span></span>

 <span data-ttu-id="91f4f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91f4f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="91f4f-108">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="91f4f-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="91f4f-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="91f4f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="91f4f-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="91f4f-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="91f4f-111">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="91f4f-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="91f4f-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="91f4f-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="91f4f-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="91f4f-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="91f4f-114">[out] Указатель на указатель на структуру возвращенные [SMAPIFormPropArray](smapiformproparray.md) .</span><span class="sxs-lookup"><span data-stu-id="91f4f-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="91f4f-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="91f4f-115">Return value</span></span>

<span data-ttu-id="91f4f-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="91f4f-116">S_OK</span></span> 
  
> <span data-ttu-id="91f4f-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="91f4f-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="91f4f-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="91f4f-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="91f4f-119">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="91f4f-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="91f4f-120">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="91f4f-120">MFCMAPI reference</span></span>

<span data-ttu-id="91f4f-121">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="91f4f-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="91f4f-122">**����**</span><span class="sxs-lookup"><span data-stu-id="91f4f-122">**File**</span></span>|<span data-ttu-id="91f4f-123">**�������**</span><span class="sxs-lookup"><span data-stu-id="91f4f-123">**Function**</span></span>|<span data-ttu-id="91f4f-124">**�����������**</span><span class="sxs-lookup"><span data-stu-id="91f4f-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91f4f-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="91f4f-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="91f4f-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="91f4f-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="91f4f-127">Mfcmapi (en) использует метод **IMAPIFormInfo::CalcFormPropSet** при записи выходных данных отладки для объекты формы.</span><span class="sxs-lookup"><span data-stu-id="91f4f-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91f4f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="91f4f-128">See also</span></span>



[<span data-ttu-id="91f4f-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="91f4f-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="91f4f-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="91f4f-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="91f4f-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="91f4f-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

