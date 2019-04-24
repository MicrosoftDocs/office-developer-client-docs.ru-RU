---
title: Итнеффинишкомпонент
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278888"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="aff1a-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="aff1a-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="aff1a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aff1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aff1a-105">Обрабатывает отдельные компоненты из сообщения по одному на один раз в поток формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="aff1a-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="aff1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aff1a-106">Parameters</span></span>

 <span data-ttu-id="aff1a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aff1a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="aff1a-108">возврата Битовая маска флагов, определяющих, какой компонент будет завершен.</span><span class="sxs-lookup"><span data-stu-id="aff1a-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="aff1a-109">Необходимо задать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="aff1a-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="aff1a-110">ТНЕФ_КОМПОНЕНТ_АТТАЧМЕНТ</span><span class="sxs-lookup"><span data-stu-id="aff1a-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="aff1a-111">Обработка будет завершена для объекта вложения; параметр _улкомпонентид_ содержит свойство **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.</span><span class="sxs-lookup"><span data-stu-id="aff1a-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="aff1a-112">ТНЕФ_КОМПОНЕНТ_МЕССАЖЕ</span><span class="sxs-lookup"><span data-stu-id="aff1a-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="aff1a-113">Обработка будет завершена для объекта Message.</span><span class="sxs-lookup"><span data-stu-id="aff1a-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="aff1a-114">_Улкомпонентид_</span><span class="sxs-lookup"><span data-stu-id="aff1a-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="aff1a-115">[in] 0 для обозначения обработки сообщения или свойства **пр_аттач_нум** вложений для обработки.</span><span class="sxs-lookup"><span data-stu-id="aff1a-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="aff1a-116">Если установлен флаг ТНЕФ_КОМПОНЕНТ_МЕССАЖЕ в параметре _ulFlags_ , _улкомпонентид_ должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="aff1a-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="aff1a-117">_Лпкустомпроплист_</span><span class="sxs-lookup"><span data-stu-id="aff1a-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="aff1a-118">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , содержащую теги свойств, которые определяют свойства, переданные в параметре _лпкустомпропс_ .</span><span class="sxs-lookup"><span data-stu-id="aff1a-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="aff1a-119">Между значением свойства в _лпкустомпропс_ и тегом свойства в параметре _лпкустомпроплист_ должно быть отношение "один к одному".</span><span class="sxs-lookup"><span data-stu-id="aff1a-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="aff1a-120">_Лпкустомпропс_</span><span class="sxs-lookup"><span data-stu-id="aff1a-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="aff1a-121">возврата Указатель на структуру [спропвалуе](spropvalue.md) , которая содержит значения свойств для кодирования.</span><span class="sxs-lookup"><span data-stu-id="aff1a-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="aff1a-122">_Лппроплист_</span><span class="sxs-lookup"><span data-stu-id="aff1a-122">_lpPropList_</span></span>
  
> <span data-ttu-id="aff1a-123">возврата Указатель на структуру **спроптагаррай** , содержащую теги свойств для кодирования свойств.</span><span class="sxs-lookup"><span data-stu-id="aff1a-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="aff1a-124">_Лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="aff1a-124">_lppProblems_</span></span>
  
> <span data-ttu-id="aff1a-125">вышли Указатель на указатель на возвращаемую структуру [стнефпроблемаррай](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="aff1a-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="aff1a-126">Структура **стнефпроблемаррай** указывает, какие свойства не кодируются должным образом.</span><span class="sxs-lookup"><span data-stu-id="aff1a-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="aff1a-127">Если параметр _лпппроблемс_ переДАЕТСЯ значение null, массив проблем свойств не возвращается.</span><span class="sxs-lookup"><span data-stu-id="aff1a-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="aff1a-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aff1a-128">Return value</span></span>

<span data-ttu-id="aff1a-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="aff1a-129">S_OK</span></span> 
  
> <span data-ttu-id="aff1a-130">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="aff1a-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aff1a-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="aff1a-131">Remarks</span></span>

<span data-ttu-id="aff1a-132">Поставщики транспорта, поставщики хранилищ сообщений и шлюзы вызывают метод **итнеф:: финишкомпонент** для выполнения обработки TNEF для одного компонента, сообщения или вложения, как показано в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="aff1a-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="aff1a-133">Чтобы включить обработку компонентов, поставщик вызова или шлюз передает флаг ТНЕФ_КОМПОНЕНТ_ЕНКОДИНГ в _ulFlags_ для функции [опентнефстреам](opentnefstream.md) или [опентнефстреамекс](opentnefstreamex.md) , открывающей объект для получения кодировки.</span><span class="sxs-lookup"><span data-stu-id="aff1a-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="aff1a-134">Передача значений в параметрах _лпкустомпроплист_ и _лпкустомпропс_ выполняет эквивалент кодирования компонентов, выполняемый методом [итнеф:: SetProps](itnef-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="aff1a-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="aff1a-135">Передача значения в параметре _лппроплист_ выполняет эквивалентную кодировку компонентов, выполняемую методом [Итнеф:: аддпропс](itnef-addprops.md) с флагом тнеф_проп_инклуде, установленным в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="aff1a-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="aff1a-136">Передача этих значений позволяет выполнять кодирование с помощью одного вызова, а не нескольких вызовов.</span><span class="sxs-lookup"><span data-stu-id="aff1a-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="aff1a-137">Реализация TNEF сообщает о неполадках кодирования потока TNEF без остановки процесса **финишкомпонент** .</span><span class="sxs-lookup"><span data-stu-id="aff1a-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="aff1a-138">Структура **стнефпроблемаррай** , возвращаемая в _лпппроблемс_ , указывает, какие АТРИБУТЫ TNEF или свойства MAPI, если они есть, не могут быть обработаны.</span><span class="sxs-lookup"><span data-stu-id="aff1a-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="aff1a-139">Значение, возвращаемое элементом **SCODE** одной из структур **стнефпроблем** , включенных в **стнефпроблемаррай** , указывает на конкретную проблему.</span><span class="sxs-lookup"><span data-stu-id="aff1a-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="aff1a-140">Поставщик или шлюз могут работать в предположении, что все свойства или атрибуты, для которых **финишкомпонент** не возвращает отчет о проблеме, были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="aff1a-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="aff1a-141">Если поставщик или шлюз не работают с неисправной массивом, он может передавать значение NULL в _лпппроблемс_; в этом случае массив проблем не возвращается.</span><span class="sxs-lookup"><span data-stu-id="aff1a-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="aff1a-142">Значение, возвращаемое в _лпппроблемс_ , является допустимым только в том случае, если вызов ВОЗВРАЩАЕТ значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="aff1a-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="aff1a-143">Когда возвращается значение S_OK, поставщик или шлюз должны проверить значения, возвращаемые в структуре [стнефпроблемаррай](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="aff1a-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="aff1a-144">Если при вызове возникает ошибка, структура **стнефпроблемаррай** не заполняется, а поставщик или шлюз вызова не должен использовать или освобождать структуру.</span><span class="sxs-lookup"><span data-stu-id="aff1a-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="aff1a-145">Если при вызове не возникнет ошибок, поставщик или шлюз вызовов должен освободить память для **стнефпроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="aff1a-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aff1a-146">См. также</span><span class="sxs-lookup"><span data-stu-id="aff1a-146">See also</span></span>



[<span data-ttu-id="aff1a-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="aff1a-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="aff1a-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="aff1a-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="aff1a-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="aff1a-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="aff1a-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="aff1a-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="aff1a-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="aff1a-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="aff1a-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="aff1a-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="aff1a-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="aff1a-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="aff1a-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aff1a-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

