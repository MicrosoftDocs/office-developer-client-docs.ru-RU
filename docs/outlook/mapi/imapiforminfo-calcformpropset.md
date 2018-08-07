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
ms.openlocfilehash: e5da9ffdd3021538ec814d1367cf1b06b49cfbc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808907"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="453ae-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="453ae-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="453ae-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="453ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="453ae-105">Возвращает указатель на полный набор свойств, используемых в форме.</span><span class="sxs-lookup"><span data-stu-id="453ae-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="453ae-106">���������</span><span class="sxs-lookup"><span data-stu-id="453ae-106">Parameters</span></span>

 <span data-ttu-id="453ae-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="453ae-107">_ulFlags_</span></span>
  
> <span data-ttu-id="453ae-108">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="453ae-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="453ae-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="453ae-109">The following flag can be set:</span></span>
    
<span data-ttu-id="453ae-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="453ae-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="453ae-111">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="453ae-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="453ae-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="453ae-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="453ae-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="453ae-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="453ae-114">[out] Указатель на указатель на структуру возвращенные [SMAPIFormPropArray](smapiformproparray.md) .</span><span class="sxs-lookup"><span data-stu-id="453ae-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="453ae-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="453ae-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="453ae-116">S_OK</span></span> 
  
> <span data-ttu-id="453ae-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="453ae-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="453ae-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="453ae-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="453ae-119">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="453ae-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="453ae-120">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="453ae-120">MFCMAPI reference</span></span>

<span data-ttu-id="453ae-121">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="453ae-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="453ae-122">**����**</span><span class="sxs-lookup"><span data-stu-id="453ae-122">**File**</span></span>|<span data-ttu-id="453ae-123">**�������**</span><span class="sxs-lookup"><span data-stu-id="453ae-123">**Function**</span></span>|<span data-ttu-id="453ae-124">**�����������**</span><span class="sxs-lookup"><span data-stu-id="453ae-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="453ae-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="453ae-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="453ae-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="453ae-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="453ae-127">Mfcmapi (en) использует метод **IMAPIFormInfo::CalcFormPropSet** при записи выходных данных отладки для объекты формы.</span><span class="sxs-lookup"><span data-stu-id="453ae-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="453ae-128">См. также</span><span class="sxs-lookup"><span data-stu-id="453ae-128">See also</span></span>



[<span data-ttu-id="453ae-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="453ae-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="453ae-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="453ae-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="453ae-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="453ae-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

