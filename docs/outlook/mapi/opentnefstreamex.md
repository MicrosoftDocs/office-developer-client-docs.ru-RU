---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406243"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="9029f-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="9029f-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="9029f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9029f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9029f-105">Создает объект Transport-Neutral формата Инкапсуляции (TNEF), который можно использовать для кодирования или декодирования объекта сообщения в поток данных TNEF для использования транспортами, шлюзами и хранилищами сообщений.</span><span class="sxs-lookup"><span data-stu-id="9029f-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="9029f-106">Это точка входа для доступа в TNEF.</span><span class="sxs-lookup"><span data-stu-id="9029f-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9029f-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9029f-107">Header file:</span></span>  <br/> |<span data-ttu-id="9029f-108">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="9029f-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="9029f-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9029f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="9029f-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9029f-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="9029f-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9029f-111">Called by:</span></span>  <br/> |<span data-ttu-id="9029f-112">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="9029f-112">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="9029f-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="9029f-113">Parameters</span></span>

<span data-ttu-id="9029f-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="9029f-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="9029f-115">[in] Передает объект поддержки или передается в NULL.</span><span class="sxs-lookup"><span data-stu-id="9029f-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="9029f-116">Если параметр NULL,  _параметр lpAddressBook_ должен иметь ненулевую заданную.</span><span class="sxs-lookup"><span data-stu-id="9029f-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="9029f-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="9029f-117">_lpStream_</span></span>
  
> <span data-ttu-id="9029f-118">[in] Указатель на объект потока хранилища, например интерфейс OLE **IStream,** предоставляющий источник или назначение для сообщения потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="9029f-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="9029f-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="9029f-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="9029f-120">[in] Указатель на имя потока данных, который использует объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="9029f-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="9029f-121">Если вызывающая группа установила флаг TNEF_ENCODE (параметр _ulFlags)_ в вызове **OpenTnefStream,** параметр  _lpszName_ должен указывать ненулевую строку, состоящую из символов, которые считаются допустимыми для именования файла.</span><span class="sxs-lookup"><span data-stu-id="9029f-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="9029f-122">MAPI не разрешает имена строк, включая символы "[", "]" или ":", даже если файловая система разрешает их использование.</span><span class="sxs-lookup"><span data-stu-id="9029f-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="9029f-123">Размер строки, передаваемой для параметра  _lpszName,_ не должен превышать значение MAX_PATH максимальной длины строки, содержаной имя пути.</span><span class="sxs-lookup"><span data-stu-id="9029f-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="9029f-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9029f-124">_ulFlags_</span></span>
  
> <span data-ttu-id="9029f-125">[in] Битоваяmas флагов, используемых для указать режим функции.</span><span class="sxs-lookup"><span data-stu-id="9029f-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="9029f-126">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9029f-126">The following flags can be set:</span></span>
    
<span data-ttu-id="9029f-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="9029f-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="9029f-128">Все возможные свойства сопоируются с их атрибутами более высокого уровня, но при возможной потере данных из-за преобразования в атрибут более высокого уровня свойство также кодируются в инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="9029f-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="9029f-129">Обратите внимание, что это приведет к дублированию информации в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="9029f-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="9029f-130">TNEF_BEST_DATA по умолчанию, если другие режимы не указаны.</span><span class="sxs-lookup"><span data-stu-id="9029f-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="9029f-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="9029f-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="9029f-132">Обеспечивает обратную совместимость с старыми клиентские приложениями.</span><span class="sxs-lookup"><span data-stu-id="9029f-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="9029f-133">Потоки TNEF, закодированные с помощью этого флага, соотят все возможные свойства с соответствующим атрибутом более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="9029f-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="9029f-134">Этот режим также приводит к стандарту некоторых свойств, которые требуются клиентам более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="9029f-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="9029f-135">Этот флаг устарел и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="9029f-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="9029f-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="9029f-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="9029f-137">Объект TNEF в заявяемом потоке открывается с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9029f-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="9029f-138">Поставщик транспорта должен установить этот флаг, если функция инициализирует объект для последующего декодирования.</span><span class="sxs-lookup"><span data-stu-id="9029f-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="9029f-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="9029f-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="9029f-140">Объект TNEF в заявяемом потоке открывается для разрешения на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="9029f-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="9029f-141">Поставщик транспорта должен установить этот флаг, если функция инициализирует объект для последующей кодии.</span><span class="sxs-lookup"><span data-stu-id="9029f-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="9029f-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="9029f-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="9029f-143">Кодирует все свойства в блоки инкапсуляции MAPI.</span><span class="sxs-lookup"><span data-stu-id="9029f-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="9029f-144">Поэтому "чистый" TNEF-файл будет состоять не более чем из атрибутов attMAPIProps, attAttachment, attRenddata и attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="9029f-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="9029f-145">Этот режим идеально подходит для использования, когда обратная совместимость не требуется.</span><span class="sxs-lookup"><span data-stu-id="9029f-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="9029f-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9029f-146">_lpMessage_</span></span>
  
> <span data-ttu-id="9029f-147">[in] Указатель на объект сообщения в качестве места назначения декодированного сообщения с вложениями или источника закодированного сообщения с вложениями.</span><span class="sxs-lookup"><span data-stu-id="9029f-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="9029f-148">Любые свойства сообщения назначения могут быть перезаписаны свойствами закодированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9029f-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="9029f-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="9029f-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="9029f-150">[in] Ключ поиска, который объект TNEF использует для поиска вложений с текстовыми тегами, вставленными в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="9029f-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="9029f-151">Это значение должно быть относительно уникальным для всех сообщений.</span><span class="sxs-lookup"><span data-stu-id="9029f-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="9029f-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="9029f-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="9029f-153">[in] Указатель на объект адресной книги, используемый для получения сведений об адресов для идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="9029f-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="9029f-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="9029f-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="9029f-155">[out] Указатель на новый объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="9029f-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9029f-156">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9029f-156">Return value</span></span>

<span data-ttu-id="9029f-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="9029f-157">S_OK</span></span> 
  
> <span data-ttu-id="9029f-158">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9029f-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9029f-159">Примечания</span><span class="sxs-lookup"><span data-stu-id="9029f-159">Remarks</span></span>

<span data-ttu-id="9029f-160">Функция **OpenTnefStreamEx** является рекомендуемой заменой [openTnefStream](opentnefstream.md), исходной точки входа для доступа в TNEF.</span><span class="sxs-lookup"><span data-stu-id="9029f-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="9029f-161">Объект TNEF, созданный функцией **OpenTnefStreamEx,** позднее вызывает метод OLE **IUnknown::AddRef,** чтобы добавить ссылки на объект поддержки, объект stream и объект сообщения.</span><span class="sxs-lookup"><span data-stu-id="9029f-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="9029f-162">Поставщик транспорта может освободить ссылки для всех трех объектов одним вызовом метода OLE **IUnknown::Release** для объекта TNEF.</span><span class="sxs-lookup"><span data-stu-id="9029f-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="9029f-163">**OpenTnefStreamEx** выделяет и инициализирует объект TNEF, который поставщик должен использовать для кодивизации сообщения MAPI в сообщение потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="9029f-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="9029f-164">Кроме того, эта функция может настроить объект поставщика для использования в последующих вызовах [ITnef::ExtractProps](itnef-extractprops.md) для декодирования сообщения потока TNEF в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="9029f-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="9029f-165">Чтобы освободить объект TNEF и закрыть сеанс, поставщик транспорта должен вызвать унаследованный метод **IUnknown::Release** объекта.</span><span class="sxs-lookup"><span data-stu-id="9029f-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="9029f-166">Базовое значение параметра _wKeyVal_ не должно быть нулем и не должно быть одинаковым для каждого вызова **OpenTnefStreamEx.**</span><span class="sxs-lookup"><span data-stu-id="9029f-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="9029f-167">Вместо этого используйте случайные числа на основе системного времени из генератора случайных чисел библиотеки времени запуска.</span><span class="sxs-lookup"><span data-stu-id="9029f-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9029f-168">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9029f-168">MFCMAPI reference</span></span>

<span data-ttu-id="9029f-169">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9029f-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9029f-170">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9029f-170">**File**</span></span>|<span data-ttu-id="9029f-171">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9029f-171">**Function**</span></span>|<span data-ttu-id="9029f-172">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9029f-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9029f-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="9029f-173">File.cpp</span></span>  <br/> |<span data-ttu-id="9029f-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="9029f-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="9029f-175">MFCMAPI использует метод **OpenTnefStreamEx** для открытия потока в TNEF-файле, чтобы можно было извлечь свойства.</span><span class="sxs-lookup"><span data-stu-id="9029f-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9029f-176">См. также</span><span class="sxs-lookup"><span data-stu-id="9029f-176">See also</span></span>

- [<span data-ttu-id="9029f-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9029f-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="9029f-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="9029f-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="9029f-179">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9029f-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

