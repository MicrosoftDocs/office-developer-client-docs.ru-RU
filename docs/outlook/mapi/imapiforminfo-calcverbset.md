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
ms.openlocfilehash: 362afb1efeddeae72cc19256c377cb2c0f7ecba0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808917"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="b9df0-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="b9df0-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="b9df0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9df0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9df0-105">Возвращает указатель на полный набор команд, которые использует формы.</span><span class="sxs-lookup"><span data-stu-id="b9df0-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="b9df0-106">���������</span><span class="sxs-lookup"><span data-stu-id="b9df0-106">Parameters</span></span>

 <span data-ttu-id="b9df0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9df0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b9df0-108">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="b9df0-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b9df0-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b9df0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="b9df0-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b9df0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b9df0-111">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="b9df0-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="b9df0-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b9df0-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b9df0-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="b9df0-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="b9df0-114">[out] Указатель на указатель на структуру возвращенные [SMAPIVerbArray](smapiverbarray.md) , содержащий команд формы.</span><span class="sxs-lookup"><span data-stu-id="b9df0-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b9df0-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b9df0-115">Return value</span></span>

<span data-ttu-id="b9df0-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b9df0-116">S_OK</span></span> 
  
> <span data-ttu-id="b9df0-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b9df0-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b9df0-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b9df0-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b9df0-119">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="b9df0-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9df0-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9df0-120">Remarks</span></span>

<span data-ttu-id="b9df0-121">Клиентские приложения вызовите метод **IMAPIFormInfo::CalcVerbSet** для получения указателя на набор команд, используемые в форме.</span><span class="sxs-lookup"><span data-stu-id="b9df0-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="b9df0-122">В структуре **SMAPIVerbArray** , возвращаемые в параметре _ppMAPIVerbArray_ команды возвращаются в порядке от номера индекса; Индекс каждой команды можно найти в его **lVerb** элементом.</span><span class="sxs-lookup"><span data-stu-id="b9df0-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="b9df0-123">Клиентские приложения могут использовать массив глаголов динамически построения меню, скрытие или отображение кнопок и так далее.</span><span class="sxs-lookup"><span data-stu-id="b9df0-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b9df0-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="b9df0-124">MFCMAPI reference</span></span>

<span data-ttu-id="b9df0-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="b9df0-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b9df0-126">**����**</span><span class="sxs-lookup"><span data-stu-id="b9df0-126">**File**</span></span>|<span data-ttu-id="b9df0-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="b9df0-127">**Function**</span></span>|<span data-ttu-id="b9df0-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="b9df0-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b9df0-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="b9df0-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="b9df0-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="b9df0-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="b9df0-131">Mfcmapi (en) использует метод **IMAPIFormInfo::CalcVerbSet** при записи выходных данных отладки для объекты формы.</span><span class="sxs-lookup"><span data-stu-id="b9df0-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9df0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="b9df0-132">See also</span></span>



[<span data-ttu-id="b9df0-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="b9df0-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="b9df0-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b9df0-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="b9df0-135">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b9df0-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

