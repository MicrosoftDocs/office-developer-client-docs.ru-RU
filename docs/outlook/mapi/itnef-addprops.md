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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396318"
---
# <a name="itnefaddprops"></a><span data-ttu-id="dde8d-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="dde8d-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="dde8d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dde8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dde8d-105">Позволяет вызова поставщика услуг или шлюза добавить свойства к инкапсуляция вложения или сообщения.</span><span class="sxs-lookup"><span data-stu-id="dde8d-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="dde8d-106">���������</span><span class="sxs-lookup"><span data-stu-id="dde8d-106">Parameters</span></span>

 <span data-ttu-id="dde8d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dde8d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dde8d-108">[in] Битовая маска флаги, который определяет, как включены или исключены из инкапсуляция свойства.</span><span class="sxs-lookup"><span data-stu-id="dde8d-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="dde8d-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="dde8d-109">The following flags can be set:</span></span>
    
<span data-ttu-id="dde8d-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="dde8d-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="dde8d-111">Кодирует только свойства с помощью параметра _lpPropList_ , являющихся частью вложения в сообщении.</span><span class="sxs-lookup"><span data-stu-id="dde8d-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="dde8d-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="dde8d-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="dde8d-113">Кодирует только свойства из вложений, указанного с помощью параметра _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="dde8d-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="dde8d-114">Если параметр _lpvData_ не может быть NULL, запись данных, на который указывает в инкапсуляция вложений в файл, указанный в свойстве **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dde8d-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="dde8d-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="dde8d-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="dde8d-116">Кодирует только свойства из сообщения или вложения, указанного с помощью параметра _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="dde8d-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="dde8d-117">Если установлен этот флаг, значение в _lpvData_ должно быть указатель [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="dde8d-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="dde8d-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="dde8d-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="dde8d-119">Кодирует все свойства не указан в параметре _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="dde8d-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="dde8d-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="dde8d-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="dde8d-121">Кодирует все свойства, указанные в _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="dde8d-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="dde8d-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="dde8d-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="dde8d-123">Кодирует только те свойства, указанные в _lpPropList_ , которые входят в состав сообщения.</span><span class="sxs-lookup"><span data-stu-id="dde8d-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="dde8d-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="dde8d-124">_ulElemID_</span></span>
  
> <span data-ttu-id="dde8d-125">[in] Свойство **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения, которое содержит число, однозначно идентифицирует вложения в сообщение его родительского.</span><span class="sxs-lookup"><span data-stu-id="dde8d-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="dde8d-126">Параметр _ulElemID_ используется при запросе специальная обработка для вложения.</span><span class="sxs-lookup"><span data-stu-id="dde8d-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="dde8d-127">Параметр _ulElemID_ должен иметь значение 0, пока флаг TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="dde8d-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dde8d-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="dde8d-128">_lpvData_</span></span>
  
> <span data-ttu-id="dde8d-129">[in] Указатель на данные вложения, используемые для замены данных вложения, указанное в _ulElemID_.</span><span class="sxs-lookup"><span data-stu-id="dde8d-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="dde8d-130">Параметр _lpvData_ должен иметь значение NULL, если не задано в _ulFlags_TNEF_PROP_CONTAINED или TNEF_PROP_CONTAINED_TNEF.</span><span class="sxs-lookup"><span data-stu-id="dde8d-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="dde8d-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="dde8d-131">_lpPropList_</span></span>
  
> <span data-ttu-id="dde8d-132">[in] Указатель на список свойств, включаемых в или исключить из инкапсуляция.</span><span class="sxs-lookup"><span data-stu-id="dde8d-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dde8d-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dde8d-133">Return value</span></span>

<span data-ttu-id="dde8d-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="dde8d-134">S_OK</span></span> 
  
> <span data-ttu-id="dde8d-135">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="dde8d-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dde8d-136">���������</span><span class="sxs-lookup"><span data-stu-id="dde8d-136">Remarks</span></span>

<span data-ttu-id="dde8d-137">Поставщики транспорта, поставщиков хранилища сообщений и шлюзов вызовите метод **ITnef::AddProps** свойств списка, чтобы быть включены или исключены из обработки Transport-Neutral Encapsulation формата TNEF сообщение или вложение.</span><span class="sxs-lookup"><span data-stu-id="dde8d-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="dde8d-138">С помощью последовательных вызовов, поставщик или шлюз можно указать список свойств для добавления и кодирования или исключить из кодирования.</span><span class="sxs-lookup"><span data-stu-id="dde8d-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="dde8d-139">Поставщики и шлюзов можно также использовать **AddProps** для предоставления правильность сведений о специальная обработка вложений.</span><span class="sxs-lookup"><span data-stu-id="dde8d-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="dde8d-140">**AddProps** поддерживается только для объектов TNEF, которые открываются с флагом TNEF_ENCODE для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="dde8d-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="dde8d-141">Обратите внимание на то, что не фактическая кодировка TNEF происходит для **AddProps** до вызова метода [ITnef::Finish](itnef-finish.md) .</span><span class="sxs-lookup"><span data-stu-id="dde8d-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="dde8d-142">Данная функциональная возможность означает, что был передан в **AddProps** указатели должны оставаться действительно до, после **завершения** вызова.</span><span class="sxs-lookup"><span data-stu-id="dde8d-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="dde8d-143">На этом этапе всех объектов и данных, переданными **AddProps** вызовы можно выпущен или освобождении.</span><span class="sxs-lookup"><span data-stu-id="dde8d-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dde8d-144">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dde8d-144">MFCMAPI reference</span></span>

<span data-ttu-id="dde8d-145">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="dde8d-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dde8d-146">**Файл**</span><span class="sxs-lookup"><span data-stu-id="dde8d-146">**File**</span></span>|<span data-ttu-id="dde8d-147">**Функция**</span><span class="sxs-lookup"><span data-stu-id="dde8d-147">**Function**</span></span>|<span data-ttu-id="dde8d-148">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="dde8d-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dde8d-149">File.cpp</span><span class="sxs-lookup"><span data-stu-id="dde8d-149">File.cpp</span></span>  <br/> |<span data-ttu-id="dde8d-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="dde8d-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="dde8d-151">Mfcmapi (en) метод **ITnef::AddProps** используется для копирования свойств из сообщения в формате TNEF поток.</span><span class="sxs-lookup"><span data-stu-id="dde8d-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dde8d-152">См. также</span><span class="sxs-lookup"><span data-stu-id="dde8d-152">See also</span></span>



[<span data-ttu-id="dde8d-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="dde8d-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="dde8d-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="dde8d-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="dde8d-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="dde8d-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="dde8d-156">Каноническое свойство PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="dde8d-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="dde8d-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dde8d-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="dde8d-158">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="dde8d-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

