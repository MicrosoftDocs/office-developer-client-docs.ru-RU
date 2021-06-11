---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348624"
---
# <a name="itnefaddprops"></a><span data-ttu-id="78781-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="78781-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="78781-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78781-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78781-105">Позволяет поставщику услуг вызова или шлюзу добавлять свойства в инкапсуляцию сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="78781-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="78781-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="78781-106">Parameters</span></span>

 <span data-ttu-id="78781-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78781-107">_ulFlags_</span></span>
  
> <span data-ttu-id="78781-108">[in] Битмашка флагов, которые контролируют, как свойства включены или исключены из инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="78781-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="78781-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="78781-109">The following flags can be set:</span></span>
    
<span data-ttu-id="78781-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="78781-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="78781-111">Кодирует только свойства в параметре  _lpPropList,_ которые являются частью вложений в сообщении.</span><span class="sxs-lookup"><span data-stu-id="78781-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="78781-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="78781-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="78781-113">Кодирует только свойства из вложения, указанного параметром _ulElemID._</span><span class="sxs-lookup"><span data-stu-id="78781-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="78781-114">Если параметр _lpvData_ не является NULL, указанные данные вписаны в инкапсуляцию вложения в файл, указанный свойством [PR_ATTACH_TRANSPORT_NAME (PidTagAttachTransportName).](pidtagattachtransportname-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="78781-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="78781-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="78781-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="78781-116">Кодирует только свойства из сообщения или вложения, указанные _параметром ulElemID._</span><span class="sxs-lookup"><span data-stu-id="78781-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="78781-117">Если задан этот флаг, значение _в lpvData_ должно быть [указателем IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)</span><span class="sxs-lookup"><span data-stu-id="78781-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="78781-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="78781-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="78781-119">Кодирует все свойства, не указанные в _параметре lpPropList._</span><span class="sxs-lookup"><span data-stu-id="78781-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="78781-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="78781-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="78781-121">Кодирует все свойства, указанные в _lpPropList._</span><span class="sxs-lookup"><span data-stu-id="78781-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="78781-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="78781-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="78781-123">Кодирует только те свойства, указанные в  _lpPropList,_ которые являются частью самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="78781-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="78781-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="78781-124">_ulElemID_</span></span>
  
> <span data-ttu-id="78781-125">[in] Свойство PR_ATTACH_NUM  [(PidTagAttachNumber),](pidtagattachnumber-canonical-property.md)которое содержит номер, который однозначно определяет вложение в родительском сообщении.</span><span class="sxs-lookup"><span data-stu-id="78781-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="78781-126">Параметр  _ulElemID_ используется при запросе специальной обработки для вложения.</span><span class="sxs-lookup"><span data-stu-id="78781-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="78781-127">Параметр _ulElemID_ должен быть 0, если флаг TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="78781-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="78781-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="78781-128">_lpvData_</span></span>
  
> <span data-ttu-id="78781-129">[in] Указатель на данные вложения, используемые для замены данных вложения, указанных в _ulElemID._</span><span class="sxs-lookup"><span data-stu-id="78781-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="78781-130">Параметр  _lpvData должен_ быть NULL, если TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="78781-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="78781-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="78781-131">_lpPropList_</span></span>
  
> <span data-ttu-id="78781-132">[in] Указатель на список свойств, которые необходимо включить или исключить из инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="78781-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78781-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78781-133">Return value</span></span>

<span data-ttu-id="78781-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="78781-134">S_OK</span></span> 
  
> <span data-ttu-id="78781-135">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="78781-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78781-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="78781-136">Remarks</span></span>

<span data-ttu-id="78781-137">Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят **методу ITnef::AddProps,** чтобы перечислить свойства, которые будут включены или исключены из формата Transport-Neutral Инкапсуляции (TNEF) обработки сообщения или вложения.</span><span class="sxs-lookup"><span data-stu-id="78781-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="78781-138">С помощью последовательных вызовов поставщик или шлюз может указать список свойств, которые необходимо добавить и кодировать или исключить из кодирования.</span><span class="sxs-lookup"><span data-stu-id="78781-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="78781-139">Поставщики и шлюзы также могут использовать **AddProps** для предоставления сведений о любых специальных вложениях обработки.</span><span class="sxs-lookup"><span data-stu-id="78781-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="78781-140">**AddProps** поддерживается только для объектов TNEF, которые открываются с TNEF_ENCODE флагом для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="78781-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="78781-141">Обратите внимание, что фактическое кодировать TNEF для **AddProps** не происходит до тех пор, пока не будет вызван метод [ITnef::Finish.](itnef-finish.md)</span><span class="sxs-lookup"><span data-stu-id="78781-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="78781-142">Эта функция означает, что указатели, переданные **в AddProps,** должны оставаться действительными до завершения вызова. </span><span class="sxs-lookup"><span data-stu-id="78781-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="78781-143">На этом этапе все объекты и данные, переданные с помощью **вызовов AddProps,** могут быть освобождены или освобождены.</span><span class="sxs-lookup"><span data-stu-id="78781-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="78781-144">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="78781-144">MFCMAPI reference</span></span>

<span data-ttu-id="78781-145">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="78781-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="78781-146">**Файл**</span><span class="sxs-lookup"><span data-stu-id="78781-146">**File**</span></span>|<span data-ttu-id="78781-147">**Функция**</span><span class="sxs-lookup"><span data-stu-id="78781-147">**Function**</span></span>|<span data-ttu-id="78781-148">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="78781-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78781-149">File.cpp</span><span class="sxs-lookup"><span data-stu-id="78781-149">File.cpp</span></span>  <br/> |<span data-ttu-id="78781-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="78781-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="78781-151">MFCMAPI использует метод **ITnef::AddProps** для копирования свойств из сообщения в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="78781-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78781-152">См. также</span><span class="sxs-lookup"><span data-stu-id="78781-152">See also</span></span>



[<span data-ttu-id="78781-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="78781-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="78781-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="78781-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="78781-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="78781-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="78781-156">Каноническое свойство PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="78781-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="78781-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78781-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="78781-158">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="78781-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

