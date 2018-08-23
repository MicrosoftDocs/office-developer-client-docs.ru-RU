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
ms.openlocfilehash: b651a913855e99e2f26dfd99fb725cc332201932
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565188"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="5e484-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="5e484-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="5e484-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e484-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e484-105">Создает объект Transport-Neutral Encapsulation формата TNEF (), который можно использовать для кодирования и декодирования объект сообщения в формате TNEF поток данных для использования с транспортов или шлюзов и хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="5e484-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="5e484-106">Это точка входа для доступа к TNEF.</span><span class="sxs-lookup"><span data-stu-id="5e484-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e484-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5e484-107">Header file:</span></span>  <br/> |<span data-ttu-id="5e484-108">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="5e484-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="5e484-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="5e484-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5e484-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e484-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e484-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="5e484-111">Called by:</span></span>  <br/> |<span data-ttu-id="5e484-112">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="5e484-112">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5e484-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e484-113">Parameters</span></span>

<span data-ttu-id="5e484-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="5e484-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="5e484-115">[in] Передает объект поддержки или передает значение NULL.</span><span class="sxs-lookup"><span data-stu-id="5e484-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="5e484-116">Если значение NULL, параметр _lpAddressBook_ должен быть не являющееся null.</span><span class="sxs-lookup"><span data-stu-id="5e484-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="5e484-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="5e484-117">_lpStream_</span></span>
  
> <span data-ttu-id="5e484-118">[in] Указатель на объект stream хранилища, например, интерфейс OLE **IStream** , предоставляя источника и назначения для потока сообщения в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="5e484-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="5e484-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="5e484-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="5e484-120">[in] Указатель на имя потока данных, который использует объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="5e484-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="5e484-121">Если вызывающего абонента есть флаг TNEF_ENCODE (параметр _ulFlags_ ) в своем вызове **OpenTnefStream**, параметр _lpszName_ необходимо указать ненулевое указатель строка ненулевое, состоящая из произвольных символов, допустимом для задания имени файла.</span><span class="sxs-lookup"><span data-stu-id="5e484-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="5e484-122">MAPI не разрешает строковые имена, включая символы «[», «]», или «:», даже если в файловой системе разрешает их использования.</span><span class="sxs-lookup"><span data-stu-id="5e484-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="5e484-123">Размер строки, переданное для параметра _lpszName_ не должно превышать значение MAX_PATH, максимальная длина строка, содержащая имя пути.</span><span class="sxs-lookup"><span data-stu-id="5e484-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="5e484-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e484-124">_ulFlags_</span></span>
  
> <span data-ttu-id="5e484-125">[in] Битовая маска флаги служит для указания режима функции.</span><span class="sxs-lookup"><span data-stu-id="5e484-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="5e484-126">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="5e484-126">The following flags can be set:</span></span>
    
<span data-ttu-id="5e484-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="5e484-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="5e484-128">Все возможные свойства сопоставляются их атрибутов нижнего уровня, но если потери данных из-за преобразования с атрибутом нижнего уровня, свойство также кодируются в encapsulations.</span><span class="sxs-lookup"><span data-stu-id="5e484-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="5e484-129">Обратите внимание на то, что это приведет к повторяющихся данных в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="5e484-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="5e484-130">Если не указаны не другие режимы TNEF_BEST_DATA значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e484-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="5e484-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="5e484-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="5e484-132">Обеспечивает обратную совместимость с более старых клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="5e484-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="5e484-133">Потоки TNEF в кодировке этот флаг будут сопоставлены с все возможные свойства их соответствующий атрибут нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="5e484-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="5e484-134">Этот режим вызывает по умолчанию некоторые свойства, необходимых для клиентов более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="5e484-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="5e484-135">Этот флаг устарел и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="5e484-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="5e484-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="5e484-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="5e484-137">Объект TNEF в указанном потоке открывается с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5e484-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="5e484-138">Поставщика транспорта должен установить этот флаг, если функция для инициализации объекта для последующих декодирования.</span><span class="sxs-lookup"><span data-stu-id="5e484-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="5e484-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="5e484-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="5e484-140">Объект TNEF в указанном потоке открывается для разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="5e484-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="5e484-141">Поставщика транспорта должен установить этот флаг, если функция для инициализации объекта для последующих кодировки.</span><span class="sxs-lookup"><span data-stu-id="5e484-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="5e484-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="5e484-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="5e484-143">Кодирует все свойства в блоки инкапсуляция MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e484-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="5e484-144">Таким образом, файл «чистая» TNEF будет состоять из, не более attMAPIProps атрибуты, attAttachment, attRenddata и attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="5e484-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="5e484-145">Этот режим идеально подходит для использования при необходимости без обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="5e484-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="5e484-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="5e484-146">_lpMessage_</span></span>
  
> <span data-ttu-id="5e484-147">[in] Указатель на объект сообщения как место назначения для декодированное сообщения с вложениями или источника для закодированного сообщения с вложениями.</span><span class="sxs-lookup"><span data-stu-id="5e484-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="5e484-148">Любые свойства назначения сообщение может быть перезаписана при свойства закодированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5e484-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="5e484-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="5e484-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="5e484-150">[in] Клавиша поиска, который использует объект TNEF в соответствии с вложениями в теги текст, вставленный в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="5e484-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="5e484-151">Это значение должно быть относительно уникальным для сообщений.</span><span class="sxs-lookup"><span data-stu-id="5e484-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="5e484-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="5e484-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="5e484-153">[in] Указатель на объект книги адрес, используемый для получения сведения об адресах для идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="5e484-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="5e484-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="5e484-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="5e484-155">[out] Указатель на новый объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="5e484-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e484-156">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="5e484-156">Return value</span></span>

<span data-ttu-id="5e484-157">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="5e484-157">S_OK</span></span> 
  
> <span data-ttu-id="5e484-158">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5e484-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e484-159">���������</span><span class="sxs-lookup"><span data-stu-id="5e484-159">Remarks</span></span>

<span data-ttu-id="5e484-160">Функция **OpenTnefStreamEx** — это рекомендуемое замены [OpenTnefStream](opentnefstream.md), исходное точки входа для доступа к TNEF.</span><span class="sxs-lookup"><span data-stu-id="5e484-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="5e484-161">Объект TNEF, созданных функцией **OpenTnefStreamEx** позднее вызывает метод OLE **IUnknown::AddRef** для добавления ссылки на объект поддержки, объект stream и объект message.</span><span class="sxs-lookup"><span data-stu-id="5e484-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="5e484-162">Поставщика транспорта можно удалить ссылки для всех трех объектов с помощью одного вызова метода OLE **функции IUnknown::Release** на объекте TNEF.</span><span class="sxs-lookup"><span data-stu-id="5e484-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="5e484-163">**OpenTnefStreamEx** выделяет и инициализирует объект TNEF для поставщика для использования в кодировке MAPI сообщения в сообщения в формате TNEF потока.</span><span class="sxs-lookup"><span data-stu-id="5e484-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="5e484-164">Кроме того эта функция настраивается объект для поставщика для использования в последующих вызовов [ITnef::ExtractProps](itnef-extractprops.md) для декодирования сообщения в формате TNEF потока в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e484-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="5e484-165">Чтобы закрыть сеанс освобождения объекта TNEF, поставщика транспорта необходимо вызвать метод унаследованные **функции IUnknown::Release** на объекте.</span><span class="sxs-lookup"><span data-stu-id="5e484-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="5e484-166">Базовое значение для параметра _wKeyVal_ не должно быть равно нулю и не должны быть одинаковыми для каждого вызова **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="5e484-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="5e484-167">Используйте случайных чисел, на основе времени системы из библиотеки времени выполнения генератор случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="5e484-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5e484-168">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="5e484-168">MFCMAPI reference</span></span>

<span data-ttu-id="5e484-169">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="5e484-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5e484-170">**����**</span><span class="sxs-lookup"><span data-stu-id="5e484-170">**File**</span></span>|<span data-ttu-id="5e484-171">**�������**</span><span class="sxs-lookup"><span data-stu-id="5e484-171">**Function**</span></span>|<span data-ttu-id="5e484-172">**�����������**</span><span class="sxs-lookup"><span data-stu-id="5e484-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e484-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="5e484-173">File.cpp</span></span>  <br/> |<span data-ttu-id="5e484-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="5e484-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="5e484-175">Mfcmapi (en) использует метод **OpenTnefStreamEx** свойства может быть извлечено открыты потока в файл формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="5e484-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e484-176">См. также</span><span class="sxs-lookup"><span data-stu-id="5e484-176">See also</span></span>

- [<span data-ttu-id="5e484-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e484-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="5e484-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="5e484-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="5e484-179">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5e484-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

