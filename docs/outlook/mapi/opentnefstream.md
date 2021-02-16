---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423960"
---
# <a name="opentnefstream"></a><span data-ttu-id="a098d-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="a098d-103">OpenTnefStream</span></span>

<span data-ttu-id="a098d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a098d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a098d-105">Вызвано поставщиком транспорта для инициировать сеанс в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="a098d-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a098d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a098d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a098d-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="a098d-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="a098d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a098d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a098d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a098d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a098d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a098d-110">Called by:</span></span>  <br/> |<span data-ttu-id="a098d-111">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="a098d-111">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="a098d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a098d-112">Parameters</span></span>

<span data-ttu-id="a098d-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="a098d-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="a098d-114">[in] Передает объект поддержки или передается в NULL.</span><span class="sxs-lookup"><span data-stu-id="a098d-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="a098d-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="a098d-115">_lpStream_</span></span>
  
> <span data-ttu-id="a098d-116">[in] Указатель на объект потока хранилища OLE **IStream,** предоставляющий источник или назначение для сообщения потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="a098d-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="a098d-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="a098d-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="a098d-118">[in] Указатель на имя потока данных, который использует объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="a098d-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="a098d-119">Если вызывающая группа установила флаг TNEF_ENCODE (параметр _ulFlags)_ в вызове **OpenTnefStream,** параметр  _lpszName_ должен указывать ненулевую строку, состоящую из любых символов, которые считаются допустимыми для именования файла.</span><span class="sxs-lookup"><span data-stu-id="a098d-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="a098d-120">MAPI не разрешает имена строк, включая символы "[", "]" или ":", даже если файловая система разрешает их использование.</span><span class="sxs-lookup"><span data-stu-id="a098d-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="a098d-121">Размер строки, передаваемой  _для lpszName,_ не должен превышать значение MAX_PATH максимальной длины строки с именем пути.</span><span class="sxs-lookup"><span data-stu-id="a098d-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="a098d-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a098d-122">_ulFlags_</span></span>
  
> <span data-ttu-id="a098d-123">[in] Битоваяmas флагов, используемых для указать режим функции.</span><span class="sxs-lookup"><span data-stu-id="a098d-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="a098d-124">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="a098d-124">The following flags can be set:</span></span>
    
<span data-ttu-id="a098d-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="a098d-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="a098d-126">Все возможные свойства сопоируются с их атрибутами более высокого уровня, но при возможной потере данных из-за преобразования в атрибут более высокого уровня свойство также кодируются в инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="a098d-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="a098d-127">Обратите внимание, что это приведет к дублированию информации в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="a098d-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="a098d-128">TNEF_BEST_DATA по умолчанию, если другие режимы не указаны.</span><span class="sxs-lookup"><span data-stu-id="a098d-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="a098d-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="a098d-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="a098d-130">Обеспечивает обратную совместимость с старыми клиентские приложениями.</span><span class="sxs-lookup"><span data-stu-id="a098d-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="a098d-131">Потоки TNEF, закодированные с помощью этого флага, соотят все возможные свойства с соответствующим атрибутом более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a098d-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="a098d-132">Этот режим также приводит к стандарту некоторых свойств, которые требуются клиентам более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a098d-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="a098d-133">Этот флаг устарел и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="a098d-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="a098d-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="a098d-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="a098d-135">Объект TNEF в заявяемом потоке открывается с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a098d-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="a098d-136">Поставщик транспорта должен установить этот флаг, если он хочет, чтобы функция инициализирует объект для последующего декодирования.</span><span class="sxs-lookup"><span data-stu-id="a098d-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="a098d-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="a098d-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="a098d-138">Объект TNEF в заявяемом потоке открыт для разрешения на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="a098d-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="a098d-139">Поставщик транспорта должен установить этот флаг, если он хочет, чтобы функция инициализирует объект для последующей кодии.</span><span class="sxs-lookup"><span data-stu-id="a098d-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="a098d-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="a098d-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="a098d-141">Кодирует все свойства в блоки инкапсуляции MAPI.</span><span class="sxs-lookup"><span data-stu-id="a098d-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="a098d-142">Поэтому "чистый" TNEF-файл будет состоять не более чем из attMAPIProps, attAttachment, attRenddata и attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="a098d-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="a098d-143">Этот режим идеально подходит для использования, когда обратная совместимость не требуется.</span><span class="sxs-lookup"><span data-stu-id="a098d-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="a098d-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="a098d-144">_lpMessage_</span></span>
  
> <span data-ttu-id="a098d-145">[in] Указатель на объект сообщения в качестве места назначения декодированного сообщения с вложениями или источника закодированного сообщения с вложениями.</span><span class="sxs-lookup"><span data-stu-id="a098d-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="a098d-146">Любые свойства сообщения назначения могут быть перезаписаны свойствами закодированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a098d-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="a098d-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="a098d-147">_wKey_</span></span>
  
> <span data-ttu-id="a098d-148">[in] Ключ поиска, который объект TNEF использует для поиска вложений с текстовыми тегами, вставленными в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="a098d-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="a098d-149">Это значение должно быть относительно уникальным для всех сообщений.</span><span class="sxs-lookup"><span data-stu-id="a098d-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="a098d-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="a098d-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="a098d-151">[out] Указатель на новый объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="a098d-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a098d-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a098d-152">Return value</span></span>

<span data-ttu-id="a098d-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="a098d-153">S_OK</span></span> 
  
> <span data-ttu-id="a098d-154">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a098d-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a098d-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="a098d-155">Remarks</span></span>

<span data-ttu-id="a098d-156">Объект TNEF, созданный функцией **OpenTnefStream,** позднее вызывает метод OLE **IUnknown::AddRef,** чтобы добавить ссылки на объект поддержки, объект stream и объект сообщения.</span><span class="sxs-lookup"><span data-stu-id="a098d-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="a098d-157">Поставщик транспорта может освободить ссылки для всех трех объектов одним вызовом метода OLE **IUnknown::Release** для объекта TNEF.</span><span class="sxs-lookup"><span data-stu-id="a098d-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="a098d-158">**OpenTnefStream** выделяет и инициализирует интерфейс **ITnef** объекта TNEF, который поставщик должен использовать при кодивке интерфейса **IMessage** сообщения MAPI в сообщение потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="a098d-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="a098d-159">Кроме того, функция может настроить объект поставщика для использования в последующих вызовах [ITnef::ExtractProps](itnef-extractprops.md) для декодирования сообщения потока TNEF в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="a098d-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="a098d-160">Чтобы освободить объект TNEF и закрыть сеанс, поставщик транспорта должен вызвать унаследованный метод **IUnknown::Release** объекта.</span><span class="sxs-lookup"><span data-stu-id="a098d-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="a098d-161">Эта функция является исходной точкой входа для доступа в TNEF и заменена [openTnefStreamEx,](opentnefstreamex.md) но по-прежнему используется для обеспечения совместимости для тех, кто уже использует TNEF.</span><span class="sxs-lookup"><span data-stu-id="a098d-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a098d-162">См. также</span><span class="sxs-lookup"><span data-stu-id="a098d-162">See also</span></span>

- [<span data-ttu-id="a098d-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a098d-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="a098d-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="a098d-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

