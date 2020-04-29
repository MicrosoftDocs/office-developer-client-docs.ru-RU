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
# <a name="opentnefstreamex"></a><span data-ttu-id="36a06-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="36a06-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="36a06-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36a06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36a06-105">Создает объект формата TNEF, который можно использовать для кодирования или декодирования объекта сообщения в поток данных TNEF для использования транспортами или шлюзами и хранилищами сообщений.</span><span class="sxs-lookup"><span data-stu-id="36a06-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="36a06-106">Это точка входа для доступа к TNEF.</span><span class="sxs-lookup"><span data-stu-id="36a06-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36a06-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="36a06-107">Header file:</span></span>  <br/> |<span data-ttu-id="36a06-108">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="36a06-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="36a06-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="36a06-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="36a06-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="36a06-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="36a06-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="36a06-111">Called by:</span></span>  <br/> |<span data-ttu-id="36a06-112">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="36a06-112">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="36a06-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="36a06-113">Parameters</span></span>

<span data-ttu-id="36a06-114">_лпвсуппорт_</span><span class="sxs-lookup"><span data-stu-id="36a06-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="36a06-115">возврата Передает объект поддержки или передает значение NULL.</span><span class="sxs-lookup"><span data-stu-id="36a06-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="36a06-116">Если значение равно NULL, параметр _лпаддрессбук_ должен иметь значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="36a06-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="36a06-117">_лпстреам_</span><span class="sxs-lookup"><span data-stu-id="36a06-117">_lpStream_</span></span>
  
> <span data-ttu-id="36a06-118">возврата Указатель на объект потока хранилища, например интерфейс OLE **IStream** , предоставляющий источник или назначение для сообщения в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="36a06-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="36a06-119">_лпсзстреамнаме_</span><span class="sxs-lookup"><span data-stu-id="36a06-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="36a06-120">возврата Указатель на имя потока данных, который использует объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="36a06-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="36a06-121">Если вызывающий абонент установил флаг TNEF_ENCODE (параметр _ulFlags_ ) в вызове **Опентнефстреам**, параметр _лпсзнаме_ должен указывать ненулевой указатель на строку со значением NULL, состоящую из любых символов, которые считаются допустимыми для имени файла.</span><span class="sxs-lookup"><span data-stu-id="36a06-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="36a06-122">MAPI не поддерживает имена строк, включая символы "[", "]" или ":", даже если файловая система разрешает их использование.</span><span class="sxs-lookup"><span data-stu-id="36a06-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="36a06-123">Размер строки, переданной для параметра _лпсзнаме_ , не должен превышать значение MAX_PATH, максимально допустимую длину строки, которая содержит имя пути.</span><span class="sxs-lookup"><span data-stu-id="36a06-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="36a06-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36a06-124">_ulFlags_</span></span>
  
> <span data-ttu-id="36a06-125">возврата Битовая маска флагов, используемых для указания режима функции.</span><span class="sxs-lookup"><span data-stu-id="36a06-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="36a06-126">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="36a06-126">The following flags can be set:</span></span>
    
<span data-ttu-id="36a06-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="36a06-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="36a06-128">Все возможные свойства сопоставляются с атрибутами нижнего уровня, но при наличии возможной потери данных из-за преобразования в атрибут нижнего уровня свойство также кодируется в инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="36a06-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="36a06-129">Обратите внимание, что это приведет к дублированию данных в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="36a06-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="36a06-130">Если другие режимы не указаны, TNEF_BEST_DATA используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36a06-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="36a06-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="36a06-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="36a06-132">Обеспечивает обратную совместимость с устаревшими клиентскими приложениями.</span><span class="sxs-lookup"><span data-stu-id="36a06-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="36a06-133">Потоки TNEF, закодированные с помощью этого флага, будут сопоставлять все возможные свойства с соответствующим атрибутом нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="36a06-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="36a06-134">В этом режиме также используются параметры по умолчанию для некоторых свойств, которые необходимы клиентам нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="36a06-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="36a06-135">Этот флаг устарел и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="36a06-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="36a06-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="36a06-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="36a06-137">Объект TNEF в указанном потоке открыт с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="36a06-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="36a06-138">Поставщик транспорта должен установить этот флаг, если функция инициализирует объект для последующего декодирования.</span><span class="sxs-lookup"><span data-stu-id="36a06-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="36a06-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="36a06-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="36a06-140">Объект TNEF в указанном потоке открыт для разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="36a06-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="36a06-141">Поставщик транспорта должен установить этот флаг, если функция инициализирует объект для последующей кодировки.</span><span class="sxs-lookup"><span data-stu-id="36a06-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="36a06-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="36a06-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="36a06-143">Кодирует все свойства в блоки инкапсуляции MAPI.</span><span class="sxs-lookup"><span data-stu-id="36a06-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="36a06-144">Таким образом, "чистый" файл TNEF будет содержать только атрибуты Аттмапипропс, Аттаттачмент, Аттренддата и АттреЦиптабле.</span><span class="sxs-lookup"><span data-stu-id="36a06-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="36a06-145">Этот режим идеально подходит для использования, если обратная совместимость не нужна.</span><span class="sxs-lookup"><span data-stu-id="36a06-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="36a06-146">_лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="36a06-146">_lpMessage_</span></span>
  
> <span data-ttu-id="36a06-147">возврата Указатель на объект Message в качестве назначения раскодированного сообщения с вложениями или источником для закодированного сообщения с вложениями.</span><span class="sxs-lookup"><span data-stu-id="36a06-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="36a06-148">Любые свойства конечного сообщения могут быть перезаписаны свойствами закодированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="36a06-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="36a06-149">_вкэйвал_</span><span class="sxs-lookup"><span data-stu-id="36a06-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="36a06-150">возврата Ключ поиска, который объект TNEF использует для согласования вложений с тегами Text, вставленными в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="36a06-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="36a06-151">Это значение должно быть относительно уникальным в сообщениях.</span><span class="sxs-lookup"><span data-stu-id="36a06-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="36a06-152">_лпаддрессбук_</span><span class="sxs-lookup"><span data-stu-id="36a06-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="36a06-153">возврата Указатель на объект адресной книги, используемый для получения сведений об адресах для идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="36a06-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="36a06-154">_лпптнеф_</span><span class="sxs-lookup"><span data-stu-id="36a06-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="36a06-155">вышли Указатель на новый объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="36a06-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36a06-156">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36a06-156">Return value</span></span>

<span data-ttu-id="36a06-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="36a06-157">S_OK</span></span> 
  
> <span data-ttu-id="36a06-158">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="36a06-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36a06-159">Примечания</span><span class="sxs-lookup"><span data-stu-id="36a06-159">Remarks</span></span>

<span data-ttu-id="36a06-160">Функция **опентнефстреамекс** является рекомендуемой заменой для [опентнефстреам](opentnefstream.md), исходной точки входа для доступа к TNEF.</span><span class="sxs-lookup"><span data-stu-id="36a06-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="36a06-161">Объект TNEF, созданный функцией **опентнефстреамекс** , вызывает метод OLE **IUnknown:: AddRef** , чтобы добавить ссылки для объекта support, объекта Stream и объекта Message.</span><span class="sxs-lookup"><span data-stu-id="36a06-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="36a06-162">Поставщик транспорта может освободить ссылки для всех трех объектов с одним вызовом метода OLE Method **IUnknown:: Release** для объекта TNEF.</span><span class="sxs-lookup"><span data-stu-id="36a06-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="36a06-163">**Опентнефстреамекс** выделяет и инициализирует объект TNEF для поставщика, который будет использоваться для кодирования сообщения MAPI в поток сообщений формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="36a06-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="36a06-164">Кроме того, эта функция может настроить объект для поставщика, который будет использоваться при последующих вызовах метода [итнеф:: екстрактпропс](itnef-extractprops.md) для декодирования сообщения потока TNEF в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="36a06-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="36a06-165">Чтобы освободить объект TNEF и закрыть сеанс, поставщик транспорта должен вызвать наследуемый метод **IUnknown:: Release** для объекта.</span><span class="sxs-lookup"><span data-stu-id="36a06-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="36a06-166">Базовое значение для параметра _вкэйвал_ не должно быть нулевым и не должно быть одинаковым для каждого вызова **опентнефстреамекс**.</span><span class="sxs-lookup"><span data-stu-id="36a06-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="36a06-167">Вместо этого используйте случайные числа на основе системного времени генератора случайных чисел библиотеки времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="36a06-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36a06-168">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36a06-168">MFCMAPI reference</span></span>

<span data-ttu-id="36a06-169">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="36a06-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36a06-170">**Файл**</span><span class="sxs-lookup"><span data-stu-id="36a06-170">**File**</span></span>|<span data-ttu-id="36a06-171">**Функция**</span><span class="sxs-lookup"><span data-stu-id="36a06-171">**Function**</span></span>|<span data-ttu-id="36a06-172">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="36a06-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36a06-173">Файл. cpp</span><span class="sxs-lookup"><span data-stu-id="36a06-173">File.cpp</span></span>  <br/> |<span data-ttu-id="36a06-174">лоадфромтнеф</span><span class="sxs-lookup"><span data-stu-id="36a06-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="36a06-175">MFCMAPI использует метод **опентнефстреамекс** , чтобы открыть поток в файле TNEF, чтобы можно было извлечь свойства.</span><span class="sxs-lookup"><span data-stu-id="36a06-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36a06-176">См. также</span><span class="sxs-lookup"><span data-stu-id="36a06-176">See also</span></span>

- [<span data-ttu-id="36a06-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="36a06-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="36a06-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="36a06-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="36a06-179">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="36a06-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

