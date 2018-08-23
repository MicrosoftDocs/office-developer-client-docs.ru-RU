---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aff805f7868ec0c2adc55ece94c45b76368ba6eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583766"
---
# <a name="itneffinish"></a><span data-ttu-id="cb124-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="cb124-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="cb124-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb124-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb124-105">По завершении обработки для всех операций Transport-Neutral Encapsulation формата TNEF в очереди и ожидание.</span><span class="sxs-lookup"><span data-stu-id="cb124-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="cb124-106">���������</span><span class="sxs-lookup"><span data-stu-id="cb124-106">Parameters</span></span>

 <span data-ttu-id="cb124-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cb124-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cb124-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="cb124-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cb124-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="cb124-109">_lpKey_</span></span>
  
> <span data-ttu-id="cb124-110">[out] Указатель на свойство key **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.</span><span class="sxs-lookup"><span data-stu-id="cb124-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="cb124-111">Объект инкапсуляция TNEF использует этот ключ в соответствии с вложением в тег размещение вложения в сообщение.</span><span class="sxs-lookup"><span data-stu-id="cb124-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="cb124-112">Этот ключ должен быть уникальным для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="cb124-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="cb124-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="cb124-113">_lpProblem_</span></span>
  
> <span data-ttu-id="cb124-114">[out] Указатель на указатель на структуру возвращенные [STnefProblemArray](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="cb124-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="cb124-115">Структура **STnefProblemArray** указывает, какие свойства при их наличии, были не кодируются должным образом.</span><span class="sxs-lookup"><span data-stu-id="cb124-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="cb124-116">Если NULL передается в параметре _lpProblem_ , возвращается массив проблема не свойство.</span><span class="sxs-lookup"><span data-stu-id="cb124-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cb124-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cb124-117">Return value</span></span>

<span data-ttu-id="cb124-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="cb124-118">S_OK</span></span> 
  
> <span data-ttu-id="cb124-119">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="cb124-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb124-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb124-120">Remarks</span></span>

<span data-ttu-id="cb124-121">Для передачи поставщиков, поставщиков хранилища сообщений и шлюзов вызова метода **ITnef::Finish** для выполнения кодирования все свойства для каких кодирования был запрошен в вызовы методов [ITnef::AddProps](itnef-addprops.md) и [ITnef::SetProps](itnef-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="cb124-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="cb124-122">Если объект TNEF был открыт с флагом TNEF_ENCODE [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) функции, метод **Готово** кодирует запрошенные свойства в поток инкапсуляция, переданный на этот объект.</span><span class="sxs-lookup"><span data-stu-id="cb124-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="cb124-123">Если объект TNEF был открыт с флагом TNEF_DECODE, метод **завершения** декодирует свойства в потоке TNEF и записывает их сообщения, которые он входит.</span><span class="sxs-lookup"><span data-stu-id="cb124-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="cb124-124">После **завершения** вызова указатель поток инкапсуляция указывает на конец данных TNEF.</span><span class="sxs-lookup"><span data-stu-id="cb124-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="cb124-125">Если поставщик или шлюз должен использовать поток данных TNEF после **завершения** вызова, его необходимо выполнить сброс указатель потока в начало поток данных TNEF.</span><span class="sxs-lookup"><span data-stu-id="cb124-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="cb124-126">Реализация TNEF отчетов проблем кодировки TNEF потока без остановки **завершения** процесса.</span><span class="sxs-lookup"><span data-stu-id="cb124-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="cb124-127">Структура [STnefProblemArray](stnefproblemarray.md) , возвращаемые в параметре _lpProblem_ указывает, какие атрибуты TNEF или свойства MAPI, если не удается обработать.</span><span class="sxs-lookup"><span data-stu-id="cb124-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="cb124-128">Значение, возвращаемое в **scode** членом одного из структур **STnefProblem** , содержащихся в **STnefProblemArray** Указывает конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="cb124-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="cb124-129">Поставщик или шлюз может работать предполагается, что все свойства или атрибуты, для которых **завершения** не возвращает отчет о проблеме обработаны успешно.</span><span class="sxs-lookup"><span data-stu-id="cb124-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="cb124-130">Если поставщик или шлюз не работает с массивами проблемы, его можно передать значение NULL в _lpProblem_; в этом случае возвращается массив не проблемы.</span><span class="sxs-lookup"><span data-stu-id="cb124-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="cb124-131">Значение, возвращаемое в _lpProblem_ действителен только в том случае, если вызов возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="cb124-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="cb124-132">Если возвращается значение S_OK, поставщик или шлюз должен проверить, значения, возвращаемые в структуре **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="cb124-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="cb124-133">При возникновении ошибки на звонок, структура **STnefProblemArray** не заполнено и вызова поставщика или шлюз не использовать или Бесплатная загрузка структуры.</span><span class="sxs-lookup"><span data-stu-id="cb124-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="cb124-134">Если ошибки не обнаружены на звонок, вызывающий поставщика или шлюз должен высвободить память для **STnefProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cb124-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cb124-135">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="cb124-135">MFCMAPI reference</span></span>

<span data-ttu-id="cb124-136">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="cb124-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cb124-137">**����**</span><span class="sxs-lookup"><span data-stu-id="cb124-137">**File**</span></span>|<span data-ttu-id="cb124-138">**�������**</span><span class="sxs-lookup"><span data-stu-id="cb124-138">**Function**</span></span>|<span data-ttu-id="cb124-139">**�����������**</span><span class="sxs-lookup"><span data-stu-id="cb124-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb124-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="cb124-140">File.cpp</span></span>  <br/> |<span data-ttu-id="cb124-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="cb124-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="cb124-142">Mfcmapi (en) использует метод **ITnef::Finish** для завершения обработки новый поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="cb124-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb124-143">См. также</span><span class="sxs-lookup"><span data-stu-id="cb124-143">See also</span></span>



[<span data-ttu-id="cb124-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="cb124-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="cb124-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="cb124-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="cb124-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="cb124-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="cb124-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="cb124-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="cb124-148">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="cb124-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="cb124-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="cb124-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="cb124-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb124-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="cb124-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="cb124-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

