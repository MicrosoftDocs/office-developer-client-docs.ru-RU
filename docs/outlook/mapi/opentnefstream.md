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
ms.openlocfilehash: 866d3be5e1c7a4375db84d1f15802e01f8d10f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810073"
---
# <a name="opentnefstream"></a><span data-ttu-id="94aee-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="94aee-103">OpenTnefStream</span></span>

<span data-ttu-id="94aee-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94aee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94aee-105">Вызывается с помощью поставщика транспорта для запуска сеанса MAPI транспорта Neutral Encapsulation формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="94aee-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94aee-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="94aee-106">Header file:</span></span>  <br/> |<span data-ttu-id="94aee-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="94aee-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="94aee-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="94aee-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="94aee-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="94aee-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="94aee-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="94aee-110">Called by:</span></span>  <br/> |<span data-ttu-id="94aee-111">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="94aee-111">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="94aee-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="94aee-112">Parameters</span></span>

<span data-ttu-id="94aee-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="94aee-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="94aee-114">[in] Передает объект поддержки или передает значение NULL.</span><span class="sxs-lookup"><span data-stu-id="94aee-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="94aee-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="94aee-115">_lpStream_</span></span>
  
> <span data-ttu-id="94aee-116">[in] Указатель на хранилище потока объекта OLE **IStream** интерфейс предоставление источника и назначения для потока сообщения в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="94aee-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="94aee-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="94aee-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="94aee-118">[in] Указатель на имя потока данных, который использует объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="94aee-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="94aee-119">Если вызывающего абонента есть флаг TNEF_ENCODE (параметр _ulFlags_ ) в своем вызове **OpenTnefStream**, параметр _lpszName_ необходимо указать ненулевое указатель строка ненулевое, состоящая из произвольных символов, допустимом для задания имени файла.</span><span class="sxs-lookup"><span data-stu-id="94aee-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="94aee-120">MAPI не разрешает строковые имена, включая символы «[», «]», или «:», даже если в файловой системе разрешает их использования.</span><span class="sxs-lookup"><span data-stu-id="94aee-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="94aee-121">Размер строки, переданное для _lpszName_ не должно превышать значение MAX_PATH, максимальная длина строка, содержащая имя пути.</span><span class="sxs-lookup"><span data-stu-id="94aee-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="94aee-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94aee-122">_ulFlags_</span></span>
  
> <span data-ttu-id="94aee-123">[in] Битовая маска флаги служит для указания режима функции.</span><span class="sxs-lookup"><span data-stu-id="94aee-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="94aee-124">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="94aee-124">The following flags can be set:</span></span>
    
<span data-ttu-id="94aee-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="94aee-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="94aee-126">Все возможные свойства сопоставляются их атрибутов нижнего уровня, но если потери данных из-за преобразования с атрибутом нижнего уровня, свойство также кодируются в encapsulations.</span><span class="sxs-lookup"><span data-stu-id="94aee-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="94aee-127">Обратите внимание на то, что это приведет к повторяющихся данных в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="94aee-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="94aee-128">Если не указаны не другие режимы TNEF_BEST_DATA значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94aee-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="94aee-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="94aee-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="94aee-130">Обеспечивает обратную совместимость с более старые клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="94aee-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="94aee-131">Потоки TNEF в кодировке этот флаг будут сопоставлены с все возможные свойства их соответствующий атрибут нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="94aee-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="94aee-132">Этот режим вызывает по умолчанию некоторые свойства, необходимых для клиентов более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="94aee-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="94aee-133">Этот флаг устарел и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="94aee-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="94aee-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="94aee-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="94aee-135">Объект TNEF в указанном потоке открывается с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="94aee-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="94aee-136">Поставщика транспорта необходимо установить этот флаг, если он хочет функции для инициализации объекта для последующих декодирования.</span><span class="sxs-lookup"><span data-stu-id="94aee-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="94aee-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="94aee-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="94aee-138">Объект TNEF в указанном потоке открывается для разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="94aee-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="94aee-139">Поставщика транспорта необходимо установить этот флаг, если он хочет функции для инициализации объекта для последующих кодировки.</span><span class="sxs-lookup"><span data-stu-id="94aee-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="94aee-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="94aee-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="94aee-141">Кодирует все свойства в блоки инкапсуляция MAPI.</span><span class="sxs-lookup"><span data-stu-id="94aee-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="94aee-142">Таким образом, файл «чистая» TNEF будет состоять из, в большинстве, attMAPIProps attAttachment, attRenddata и attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="94aee-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="94aee-143">Этот режим идеально подходит для использования при необходимости без обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="94aee-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="94aee-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="94aee-144">_lpMessage_</span></span>
  
> <span data-ttu-id="94aee-145">[in] Указатель на объект сообщения как место назначения для декодированное сообщения с вложениями или источника для закодированного сообщения с вложениями.</span><span class="sxs-lookup"><span data-stu-id="94aee-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="94aee-146">Любые свойства назначения сообщения могут быть перезаписаны по свойствам закодированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="94aee-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="94aee-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="94aee-147">_wKey_</span></span>
  
> <span data-ttu-id="94aee-148">[in] Клавиша поиска, который использует объект TNEF в соответствии с вложениями в теги текст, вставленный в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="94aee-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="94aee-149">Это значение должно быть относительно уникальным для сообщений.</span><span class="sxs-lookup"><span data-stu-id="94aee-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="94aee-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="94aee-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="94aee-151">[out] Указатель на новый объект TNEF.</span><span class="sxs-lookup"><span data-stu-id="94aee-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94aee-152">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="94aee-152">Return value</span></span>

<span data-ttu-id="94aee-153">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="94aee-153">S_OK</span></span> 
  
> <span data-ttu-id="94aee-154">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="94aee-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94aee-155">���������</span><span class="sxs-lookup"><span data-stu-id="94aee-155">Remarks</span></span>

<span data-ttu-id="94aee-156">Объект TNEF, созданных функцией **OpenTnefStream** позднее вызывает метод OLE **IUnknown::AddRef** для добавления ссылки на объект поддержки, объект stream и объект message.</span><span class="sxs-lookup"><span data-stu-id="94aee-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="94aee-157">Поставщика транспорта можно удалить ссылки для всех трех объектов с помощью одного вызова метода OLE **функции IUnknown::Release** на объекте TNEF.</span><span class="sxs-lookup"><span data-stu-id="94aee-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="94aee-158">**OpenTnefStream** выделяет и инициализирует интерфейсом **ITnef** объект TNEF для поставщика для использования в кодировке **IMessage** интерфейсом MAPI сообщения в сообщения в формате TNEF потока.</span><span class="sxs-lookup"><span data-stu-id="94aee-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="94aee-159">Кроме того функции можно задать объект для поставщика для использования в последующих вызовов [ITnef::ExtractProps](itnef-extractprops.md) для декодирования сообщения в формате TNEF потока в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="94aee-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="94aee-160">Чтобы закрыть сеанс освобождения объекта TNEF, поставщика транспорта необходимо вызвать метод унаследованные **функции IUnknown::Release** на объекте.</span><span class="sxs-lookup"><span data-stu-id="94aee-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="94aee-161">Эта функция — это исходное точки входа для доступа к TNEF и вместо нее [OpenTnefStreamEx](opentnefstreamex.md) , но по-прежнему используется для обеспечения совместимости для тех, кто уже использует TNEF.</span><span class="sxs-lookup"><span data-stu-id="94aee-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94aee-162">См. также</span><span class="sxs-lookup"><span data-stu-id="94aee-162">See also</span></span>

- [<span data-ttu-id="94aee-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94aee-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="94aee-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="94aee-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

