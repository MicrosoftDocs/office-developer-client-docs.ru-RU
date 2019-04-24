---
title: Итнеффиниш
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348589"
---
# <a name="itneffinish"></a><span data-ttu-id="f604d-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="f604d-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="f604d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f604d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f604d-105">Заканчивает обработку для всех операций с отправкой в формате инкапсуляции (TNEF), которые находятся в очереди и ожидают.</span><span class="sxs-lookup"><span data-stu-id="f604d-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="f604d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f604d-106">Parameters</span></span>

 <span data-ttu-id="f604d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f604d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f604d-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="f604d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f604d-109">_Лпкэй_</span><span class="sxs-lookup"><span data-stu-id="f604d-109">_lpKey_</span></span>
  
> <span data-ttu-id="f604d-110">вышли Указатель на свойство ключа **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.</span><span class="sxs-lookup"><span data-stu-id="f604d-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="f604d-111">Объект инкапсуляции TNEF использует этот ключ для согласования вложения с тегом размещения вложений в сообщении.</span><span class="sxs-lookup"><span data-stu-id="f604d-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="f604d-112">Этот ключ должен быть уникальным для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="f604d-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="f604d-113">_Лппроблем_</span><span class="sxs-lookup"><span data-stu-id="f604d-113">_lpProblem_</span></span>
  
> <span data-ttu-id="f604d-114">вышли Указатель на указатель на возвращаемую структуру [стнефпроблемаррай](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="f604d-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="f604d-115">Структура **стнефпроблемаррай** указывает, какие свойства не кодируются должным образом.</span><span class="sxs-lookup"><span data-stu-id="f604d-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="f604d-116">Если параметр _лппроблем_ переДАЕТСЯ значение null, массив проблем свойств не возвращается.</span><span class="sxs-lookup"><span data-stu-id="f604d-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f604d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f604d-117">Return value</span></span>

<span data-ttu-id="f604d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f604d-118">S_OK</span></span> 
  
> <span data-ttu-id="f604d-119">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="f604d-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f604d-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="f604d-120">Remarks</span></span>

<span data-ttu-id="f604d-121">Поставщики транспорта, поставщики хранилищ сообщений и шлюзы вызывают метод **итнеф:: Finish** для выполнения кодирования всех свойств, для которых была запрошена кодировка при вызовах методов [Итнеф:: аддпропс](itnef-addprops.md) и [итнеф:: SetProps](itnef-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="f604d-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="f604d-122">Если объект TNEF был открыт с флагом ТНЕФ_ЕНКОДЕ для функции [опентнефстреам](opentnefstream.md) или [Опентнефстреамекс](opentnefstreamex.md) , метод **Finish** кодирует запрошенные свойства в поток инкапсуляции, переданный в этот объект.</span><span class="sxs-lookup"><span data-stu-id="f604d-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="f604d-123">Если объект TNEF был открыт с флагом ТНЕФ_ДЕКОДЕ, метод **Finish** декодирует свойства из потока TNEF и записывает их обратно в сообщение, к которому они принадлежат.</span><span class="sxs-lookup"><span data-stu-id="f604d-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="f604d-124">По завершении вызова указатель на поток инкапсуляции указывает на конец данных TNEF. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f604d-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="f604d-125">Если поставщик или шлюз должен использовать данные потока TNEF после вызова метода **Finish** , он должен сбросить указатель потока к началу данных потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="f604d-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="f604d-126">Реализация TNEF сообщает о неполадках кодирования потока TNEF без остановки процесса **завершения** .</span><span class="sxs-lookup"><span data-stu-id="f604d-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="f604d-127">Структура [стнефпроблемаррай](stnefproblemarray.md) , возвращаемая параметром _лппроблем_ , указывает, какие АТРИБУТЫ TNEF или свойства MAPI, если они есть, не могут быть обработаны.</span><span class="sxs-lookup"><span data-stu-id="f604d-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="f604d-128">Значение, возвращаемое элементом **SCODE** одной из структур **стнефпроблем** , включенных в **стнефпроблемаррай** , указывает на конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="f604d-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="f604d-129">Поставщик или шлюз могут работать в предположении, что все свойства или атрибуты, для \*\*\*\* которых не возвращается отчет о проблеме, были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="f604d-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="f604d-130">Если поставщик или шлюз не работают с неисправной массивом, он может передавать значение NULL в _лппроблем_; в этом случае массив проблем не возвращается.</span><span class="sxs-lookup"><span data-stu-id="f604d-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="f604d-131">Значение, возвращаемое в _лппроблем_ , является допустимым только в том случае, если вызов ВОЗВРАЩАЕТ значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="f604d-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="f604d-132">Когда возвращается значение S_OK, поставщик или шлюз должны проверить значения, возвращаемые в структуре **стнефпроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="f604d-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="f604d-133">Если при вызове возникает ошибка, структура **стнефпроблемаррай** не заполняется, а поставщик или шлюз вызова не должен использовать или освобождать структуру.</span><span class="sxs-lookup"><span data-stu-id="f604d-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="f604d-134">Если при вызове не возникнет ошибок, поставщик или шлюз вызовов должен освободить память для **стнефпроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f604d-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f604d-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f604d-135">MFCMAPI reference</span></span>

<span data-ttu-id="f604d-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f604d-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f604d-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f604d-137">**File**</span></span>|<span data-ttu-id="f604d-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f604d-138">**Function**</span></span>|<span data-ttu-id="f604d-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f604d-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f604d-140">Файл. cpp</span><span class="sxs-lookup"><span data-stu-id="f604d-140">File.cpp</span></span>  <br/> |<span data-ttu-id="f604d-141">Саветотнеф</span><span class="sxs-lookup"><span data-stu-id="f604d-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="f604d-142">MFCMAPI использует метод **итнеф:: Finish** для завершения обработки нового потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="f604d-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f604d-143">См. также</span><span class="sxs-lookup"><span data-stu-id="f604d-143">See also</span></span>



[<span data-ttu-id="f604d-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="f604d-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="f604d-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f604d-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f604d-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="f604d-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="f604d-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="f604d-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="f604d-148">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="f604d-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="f604d-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="f604d-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="f604d-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f604d-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="f604d-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f604d-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

