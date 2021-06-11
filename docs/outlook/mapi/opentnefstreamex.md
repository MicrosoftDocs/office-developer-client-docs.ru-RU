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
# <a name="opentnefstreamex"></a><span data-ttu-id="09a3e-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="09a3e-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="09a3e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09a3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09a3e-105">Создает объект Transport-Neutral формата Инкапсуляции (TNEF), который можно использовать для кодирования или декодирования объекта сообщения в поток данных TNEF для использования транспортными средствами или шлюзами и хранилищами сообщений.</span><span class="sxs-lookup"><span data-stu-id="09a3e-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="09a3e-106">Это точка входа для доступа к TNEF.</span><span class="sxs-lookup"><span data-stu-id="09a3e-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09a3e-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="09a3e-107">Header file:</span></span>  <br/> |<span data-ttu-id="09a3e-108">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="09a3e-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="09a3e-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="09a3e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="09a3e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="09a3e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="09a3e-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="09a3e-111">Called by:</span></span>  <br/> |<span data-ttu-id="09a3e-112">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="09a3e-112">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="09a3e-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="09a3e-113">Parameters</span></span>

<span data-ttu-id="09a3e-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="09a3e-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="09a3e-115">[in] Передает объект поддержки или передается в NULL.</span><span class="sxs-lookup"><span data-stu-id="09a3e-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="09a3e-116">Если NULL, параметр  _lpAddressBook_ должен быть ненульным.</span><span class="sxs-lookup"><span data-stu-id="09a3e-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="09a3e-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="09a3e-117">_lpStream_</span></span>
  
> <span data-ttu-id="09a3e-118">[in] Указатель на объект потока хранения, например интерфейс OLE **IStream,** предоставляющий источник или назначение для сообщения потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="09a3e-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="09a3e-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="09a3e-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="09a3e-120">[in] Указатель на имя потока данных, который использует объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="09a3e-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="09a3e-121">Если вызывающий вызов **в OpenTnefStream** задает флаг TNEF_ENCODE _(параметр ulFlags),_ параметр _lpszName_ должен указать указатель non-null на строку non-null, состоящую из символов, которые считаются допустимыми для именования файла.</span><span class="sxs-lookup"><span data-stu-id="09a3e-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="09a3e-122">MAPI не разрешает строковые имена, включая символы "[",]" или ":", даже если файловая система разрешает их использование.</span><span class="sxs-lookup"><span data-stu-id="09a3e-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="09a3e-123">Размер строки, переданной для параметра  _lpszName,_ не должен превышать значение MAX_PATH, максимальной длины строки с именем пути.</span><span class="sxs-lookup"><span data-stu-id="09a3e-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="09a3e-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09a3e-124">_ulFlags_</span></span>
  
> <span data-ttu-id="09a3e-125">[in] Bitmask флагов, используемых для указать режим функции.</span><span class="sxs-lookup"><span data-stu-id="09a3e-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="09a3e-126">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="09a3e-126">The following flags can be set:</span></span>
    
<span data-ttu-id="09a3e-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="09a3e-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="09a3e-128">Все возможные свойства отображутся в атрибуты вниз по уровню, но при возможной потере данных из-за преобразования в атрибут down-level свойство также закодируется в инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="09a3e-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="09a3e-129">Обратите внимание, что это приведет к дублированию сведений в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="09a3e-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="09a3e-130">TNEF_BEST_DATA по умолчанию, если другие режимы не указаны.</span><span class="sxs-lookup"><span data-stu-id="09a3e-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="09a3e-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="09a3e-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="09a3e-132">Обеспечивает обратную совместимость с более старыми клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="09a3e-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="09a3e-133">Потоки TNEF, закодированные с помощью этого флага, соотносят все возможные свойства в соответствующий атрибут ниже уровня.</span><span class="sxs-lookup"><span data-stu-id="09a3e-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="09a3e-134">Этот режим также вызывает дефолт некоторых свойств, которые требуются клиентами на более высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="09a3e-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="09a3e-135">Этот флаг устарел и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="09a3e-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="09a3e-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="09a3e-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="09a3e-137">Объект TNEF в указанный поток открывается только для чтения.</span><span class="sxs-lookup"><span data-stu-id="09a3e-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="09a3e-138">Поставщик транспорта должен установить этот флаг, если функция инициализирует объект для последующей декодирования.</span><span class="sxs-lookup"><span data-stu-id="09a3e-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="09a3e-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="09a3e-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="09a3e-140">Объект TNEF в указанный поток открыт для разрешения на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="09a3e-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="09a3e-141">Поставщик транспорта должен установить этот флаг, если функция инициализирует объект для последующего кодинга.</span><span class="sxs-lookup"><span data-stu-id="09a3e-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="09a3e-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="09a3e-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="09a3e-143">Кодирует все свойства в блоки инкапсуляции MAPI.</span><span class="sxs-lookup"><span data-stu-id="09a3e-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="09a3e-144">Таким образом, "чистый" TNEF-файл будет состоять как минимум из атрибутов attMAPIProps, attAttachment, attRenddata и attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="09a3e-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="09a3e-145">Этот режим идеально подходит для использования, если не требуется обратная совместимость.</span><span class="sxs-lookup"><span data-stu-id="09a3e-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="09a3e-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="09a3e-146">_lpMessage_</span></span>
  
> <span data-ttu-id="09a3e-147">[in] Указатель на объект сообщения в качестве назначения декодированного сообщения с вложениями или источника закодированного сообщения с вложениями.</span><span class="sxs-lookup"><span data-stu-id="09a3e-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="09a3e-148">Любые свойства сообщения назначения могут быть перезаписаны свойствами закодированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="09a3e-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="09a3e-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="09a3e-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="09a3e-150">[in] Ключ поиска, который используется объектом TNEF для совпадения вложений с текстовыми тегами, вставленными в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="09a3e-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="09a3e-151">Это значение должно быть относительно уникальным для всех сообщений.</span><span class="sxs-lookup"><span data-stu-id="09a3e-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="09a3e-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="09a3e-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="09a3e-153">[in] Указатель на объект адресной книги, используемый для получения адресных сведений для идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="09a3e-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="09a3e-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="09a3e-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="09a3e-155">[вышел] Указатель на новый объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="09a3e-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09a3e-156">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09a3e-156">Return value</span></span>

<span data-ttu-id="09a3e-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="09a3e-157">S_OK</span></span> 
  
> <span data-ttu-id="09a3e-158">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="09a3e-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09a3e-159">Примечания</span><span class="sxs-lookup"><span data-stu-id="09a3e-159">Remarks</span></span>

<span data-ttu-id="09a3e-160">Функция **OpenTnefStreamEx** является рекомендуемой заменой [openTnefStream](opentnefstream.md)— исходной точки входа для доступа к TNEF.</span><span class="sxs-lookup"><span data-stu-id="09a3e-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="09a3e-161">Объект TNEF, созданный функцией **OpenTnefStreamEx,** позднее вызывает метод **OLE IUnknown::AddRef** для добавления ссылок для объекта поддержки, объекта потока и объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="09a3e-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="09a3e-162">Поставщик транспорта может выпустить ссылки для всех трех объектов одним вызовом на метод **OLE IUnknown::Release** на объекте TNEF.</span><span class="sxs-lookup"><span data-stu-id="09a3e-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="09a3e-163">**OpenTnefStreamEx** выделяет и инициализует объект TNEF, который поставщик использует для кодификинга сообщения MAPI в сообщение потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="09a3e-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="09a3e-164">Кроме того, эта функция может настроить объект для поставщика для использования в последующих вызовах [в ITnef::ExtractProps](itnef-extractprops.md) для декодирования сообщения потока TNEF в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="09a3e-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="09a3e-165">Чтобы освободить объект TNEF и закрыть сеанс, поставщик транспорта должен вызвать унаследованный **метод IUnknown::Release** на объекте.</span><span class="sxs-lookup"><span data-stu-id="09a3e-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="09a3e-166">Базовое значение параметра _wKeyVal_ не должно быть нулевым и не должно быть одинаковым для каждого звонка **в OpenTnefStreamEx.**</span><span class="sxs-lookup"><span data-stu-id="09a3e-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="09a3e-167">Вместо этого используйте случайные числа в зависимости от системного времени из генератора случайных чисел библиотеки.</span><span class="sxs-lookup"><span data-stu-id="09a3e-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09a3e-168">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="09a3e-168">MFCMAPI reference</span></span>

<span data-ttu-id="09a3e-169">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="09a3e-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09a3e-170">**Файл**</span><span class="sxs-lookup"><span data-stu-id="09a3e-170">**File**</span></span>|<span data-ttu-id="09a3e-171">**Функция**</span><span class="sxs-lookup"><span data-stu-id="09a3e-171">**Function**</span></span>|<span data-ttu-id="09a3e-172">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="09a3e-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09a3e-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="09a3e-173">File.cpp</span></span>  <br/> |<span data-ttu-id="09a3e-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="09a3e-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="09a3e-175">MFCMAPI использует метод **OpenTnefStreamEx** для открытия потока в файле TNEF, чтобы можно было извлечь свойства.</span><span class="sxs-lookup"><span data-stu-id="09a3e-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09a3e-176">См. также</span><span class="sxs-lookup"><span data-stu-id="09a3e-176">See also</span></span>

- [<span data-ttu-id="09a3e-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="09a3e-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="09a3e-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="09a3e-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="09a3e-179">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="09a3e-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

