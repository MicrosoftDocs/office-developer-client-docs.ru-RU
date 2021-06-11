---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428783"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="4bbe3-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="4bbe3-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="4bbe3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bbe3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bbe3-105">Возвращает указатель к полному набору глаголов, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="4bbe3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4bbe3-106">Parameters</span></span>

 <span data-ttu-id="4bbe3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4bbe3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4bbe3-108">[in] Битмашка флагов, контролируемая типом возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="4bbe3-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="4bbe3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="4bbe3-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4bbe3-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4bbe3-111">Возвращенные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="4bbe3-112">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="4bbe3-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="4bbe3-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="4bbe3-114">[вышел] Указатель на указатель на возвращенную [структуру SMAPIVerbArray,](smapiverbarray.md) которая содержит глаголы формы.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4bbe3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bbe3-115">Return value</span></span>

<span data-ttu-id="4bbe3-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4bbe3-116">S_OK</span></span> 
  
> <span data-ttu-id="4bbe3-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4bbe3-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="4bbe3-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4bbe3-119">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4bbe3-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="4bbe3-120">Remarks</span></span>

<span data-ttu-id="4bbe3-121">Клиентские приложения звонят по методу **IMAPIFormInfo::CalcVerbSet,** чтобы получить указатель на набор глаголов, используемых формой.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="4bbe3-122">В **структуре SMAPIVerbArray,** возвращаемой в параметре _ppMAPIVerbArray,_ глаголы возвращаются в порядке номера индекса; Индекс каждого глагола находится в его **члене lVerb.**</span><span class="sxs-lookup"><span data-stu-id="4bbe3-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="4bbe3-123">Клиентские приложения могут использовать массив глаголов для динамической сборки меню, сокрытия или показа кнопок и так далее.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4bbe3-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4bbe3-124">MFCMAPI reference</span></span>

<span data-ttu-id="4bbe3-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4bbe3-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="4bbe3-126">**File**</span></span>|<span data-ttu-id="4bbe3-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="4bbe3-127">**Function**</span></span>|<span data-ttu-id="4bbe3-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="4bbe3-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4bbe3-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="4bbe3-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="4bbe3-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="4bbe3-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="4bbe3-131">MFCMAPI использует **метод IMAPIFormInfo::CalcVerbSet** при написании вывода отлаговки для информационных объектов форм.</span><span class="sxs-lookup"><span data-stu-id="4bbe3-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4bbe3-132">См. также</span><span class="sxs-lookup"><span data-stu-id="4bbe3-132">See also</span></span>



[<span data-ttu-id="4bbe3-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="4bbe3-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="4bbe3-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4bbe3-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="4bbe3-135">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="4bbe3-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

