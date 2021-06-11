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
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435679"
---
# <a name="itneffinish"></a><span data-ttu-id="f7fa3-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="f7fa3-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="f7fa3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7fa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7fa3-105">Завершает обработку всех операций Transport-Neutral формата Инкапсуляции (TNEF), которые находятся в очереди и ожидаются.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="f7fa3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f7fa3-106">Parameters</span></span>

 <span data-ttu-id="f7fa3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7fa3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f7fa3-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f7fa3-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="f7fa3-109">_lpKey_</span></span>
  
> <span data-ttu-id="f7fa3-110">[вышел] Указатель на ключевое **свойство PR_ATTACH_NUM** [(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f7fa3-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="f7fa3-111">Объект инкапсуляции TNEF использует этот ключ для совпадения вложения с тегом размещения вложения в сообщении.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="f7fa3-112">Этот ключ должен быть уникальным для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="f7fa3-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="f7fa3-113">_lpProblem_</span></span>
  
> <span data-ttu-id="f7fa3-114">[вышел] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="f7fa3-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="f7fa3-115">Структура **STnefProblemArray** указывает, какие свойства, если таковые имеются, были неправильно закодированы.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="f7fa3-116">Если NULL передается в  _параметре lpProblem,_ массив проблем свойств не возвращается.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f7fa3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7fa3-117">Return value</span></span>

<span data-ttu-id="f7fa3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7fa3-118">S_OK</span></span> 
  
> <span data-ttu-id="f7fa3-119">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7fa3-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7fa3-120">Remarks</span></span>

<span data-ttu-id="f7fa3-121">Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят по методу **ITnef:::Finish** для выполнения кодификинга всех свойств, для которых кодировока запрашивалась в вызовах в методы [ITnef::AddProps](itnef-addprops.md) и [ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="f7fa3-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="f7fa3-122">Если объект TNEF был открыт с флагом TNEF_ENCODE для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx,](opentnefstreamex.md) метод **Finish** кодирует запрашиваемую свойства в поток инкапсуляции, переданный этому объекту.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="f7fa3-123">Если объект TNEF был открыт с флагом TNEF_DECODE, метод **Finish** декодирует свойства из потока TNEF и записывает их обратно в принадлежаное им сообщение.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="f7fa3-124">После завершения **вызова** указатель на поток инкапсуляции указывает на конец данных TNEF.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="f7fa3-125">Если поставщику или шлюзу необходимо использовать данные  потока TNEF после завершения вызова, он должен сбросить указатель потока к началу данных потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="f7fa3-126">Реализация TNEF сообщает о проблемах кодификации потока TNEF без остановки **процесса завершения.**</span><span class="sxs-lookup"><span data-stu-id="f7fa3-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="f7fa3-127">Структура [STnefProblemArray,](stnefproblemarray.md) возвращаемая в  _параметре lpProblem,_ указывает, какие атрибуты TNEF или свойства MAPI, если таковые имеются, не удалось обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="f7fa3-128">Значение, возвращаемого  в члене кода одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="f7fa3-129">Поставщик или шлюз могут работать с предположением, что все свойства или атрибуты, для которых **Finish** не возвращает отчет о проблеме, были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="f7fa3-130">Если поставщик или шлюз не работают с массивами проблем, он может передать NULL в  _lpProblem;_ В этом случае массив проблем не возвращается.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="f7fa3-131">Возвращаемая в  _lpProblem_ величина действительна только в том случае, если вызов возвращается S_OK.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="f7fa3-132">Когда S_OK возвращается, поставщик или шлюз должны проверить значения, возвращенные в **структуре STnefProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="f7fa3-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="f7fa3-133">Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, а поставщик вызовов или шлюз не должен использовать или освободить структуру.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="f7fa3-134">Если при вызове не возникает ошибки, поставщик вызовов или шлюз должен освободить память **для STnefProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="f7fa3-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f7fa3-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f7fa3-135">MFCMAPI reference</span></span>

<span data-ttu-id="f7fa3-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f7fa3-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f7fa3-137">**File**</span></span>|<span data-ttu-id="f7fa3-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f7fa3-138">**Function**</span></span>|<span data-ttu-id="f7fa3-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f7fa3-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7fa3-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="f7fa3-140">File.cpp</span></span>  <br/> |<span data-ttu-id="f7fa3-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="f7fa3-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="f7fa3-142">MFCMAPI использует метод **ITnef::Finish** для завершения обработки нового потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="f7fa3-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7fa3-143">См. также</span><span class="sxs-lookup"><span data-stu-id="f7fa3-143">See also</span></span>



[<span data-ttu-id="f7fa3-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="f7fa3-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="f7fa3-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f7fa3-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f7fa3-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="f7fa3-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="f7fa3-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="f7fa3-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="f7fa3-148">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="f7fa3-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="f7fa3-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="f7fa3-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="f7fa3-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7fa3-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="f7fa3-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f7fa3-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

