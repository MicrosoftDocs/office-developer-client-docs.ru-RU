---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406523"
---
# <a name="openimsgonistg"></a><span data-ttu-id="e2623-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="e2623-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="e2623-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2623-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2623-105">Создает новый объект [IMessage](imessageimapiprop.md) поверх существующего объекта OLE **IStorage,** который будет использоваться в сеансе сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2623-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2623-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e2623-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2623-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="e2623-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e2623-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e2623-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e2623-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e2623-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e2623-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e2623-110">Called by:</span></span>  <br/> |<span data-ttu-id="e2623-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="e2623-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a><span data-ttu-id="e2623-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2623-112">Parameters</span></span>

<span data-ttu-id="e2623-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="e2623-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="e2623-114">[in] Указатель на объект сеанса сообщения, в котором должен быть создан новый объект **IMessage** **-on-IStorage.**</span><span class="sxs-lookup"><span data-stu-id="e2623-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="e2623-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e2623-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e2623-116">[in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="e2623-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="e2623-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e2623-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e2623-118">[in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="e2623-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="e2623-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e2623-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e2623-120">[in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память.</span><span class="sxs-lookup"><span data-stu-id="e2623-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="e2623-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="e2623-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="e2623-122">[in] Указатель на объект-память для размещения интерфейса OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="e2623-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="e2623-123">Интерфейс **IMessage** должен использовать этот метод выделения при работе с такими интерфейсами, как **IStorage** и **IStream.**</span><span class="sxs-lookup"><span data-stu-id="e2623-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="e2623-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="e2623-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="e2623-125">[in] Необязательный указатель на объект поддержки MAPI, который поставщик службы может использовать для вызова методов [интерфейса IMAPISupport : IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="e2623-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="e2623-126">_lpStg_</span></span>
  
> <span data-ttu-id="e2623-127">[in, out] Указатель на открытый объект OLE **IStorage** с разрешением только для чтения или чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e2623-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="e2623-128">Так **как IMessage** не поддерживает доступ только для записи, **OpenIMsgOnIStg** не принимает объект хранилища, открытый в режиме только для записи.</span><span class="sxs-lookup"><span data-stu-id="e2623-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="e2623-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="e2623-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="e2623-130">[in] Необязательный указатель на функцию вызова на основе прототипа [MSGCALLRELEASE,](msgcallrelease.md) который MAPI должен вызывать после последнего выпуска объекта **IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="e2623-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="e2623-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="e2623-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="e2623-132">[in] Данные вызываемого объекта, сохраненные с помощью MAPI с объектом **IMessage** **-on-IStorage** и переданные функции вызова на основе **MSGCALLRELEASE.**</span><span class="sxs-lookup"><span data-stu-id="e2623-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="e2623-133">Данные предоставляют контекст об **освобожденных объектах IMessage** и **объекте IStorage,** поверх которого он был создан.</span><span class="sxs-lookup"><span data-stu-id="e2623-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="e2623-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2623-134">_ulFlags_</span></span>
  
> <span data-ttu-id="e2623-135">[in] Битовая почта флагов, используемая для управления вызовом метода OLE **IStorage::Commit,** когда клиентские приложения или поставщик службы вызывает метод **IMessage::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="e2623-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="e2623-136">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e2623-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="e2623-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="e2623-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="e2623-138">Метод OLE **IStorage::Commit** не вызывается, когда клиент или поставщик вызывает [SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="e2623-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2623-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="e2623-140">Позволяет создавать MSG-файлы Юникода.</span><span class="sxs-lookup"><span data-stu-id="e2623-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="e2623-141">В [итоговом файле IMessage](imessageimapiprop.md) STORE_UNICODE_OK в [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) поддерживаются свойства Юникод.</span><span class="sxs-lookup"><span data-stu-id="e2623-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="e2623-142">Флаг MAPI_UNICODE поддерживается только в этой функции в Outlook 2003 или более высоких уровнях.</span><span class="sxs-lookup"><span data-stu-id="e2623-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="e2623-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="e2623-143">_lppMsg_</span></span>
  
> <span data-ttu-id="e2623-144">[out] Указатель на указатель на открытый **объект IMessage.**</span><span class="sxs-lookup"><span data-stu-id="e2623-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e2623-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2623-145">Return value</span></span>

<span data-ttu-id="e2623-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2623-146">S_OK</span></span> 
  
> <span data-ttu-id="e2623-147">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="e2623-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2623-148">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2623-148">Remarks</span></span>

<span data-ttu-id="e2623-149">Доступ к атрибутам свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="e2623-150">Чтобы сделать свойства MAPI доступными для объекта OLE структурированного хранилища, **OpenIMsgOnIStg** создает [объект IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="e2623-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="e2623-151">Атрибуты свойств для таких объектов можно установить или изменить с помощью [SetAttribIMsgOnIStg](setattribimsgonistg.md) и получить с помощью [GetAttribIMsgOnIStg.](getattribimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2623-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e2623-152">Notes to callers</span></span>

<span data-ttu-id="e2623-153">Перед тем как будет вызван **OpenIMsgOnIStg,** необходимо открыть сеанс сообщения с помощью [OpenIMsgSession.](openimsgsession.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="e2623-154">Если предоставить допустимый  _параметр lpMsgSess,_ новое сообщение будет создано в течение сеанса сообщения, чтобы оно было закрыто при закрытии сеанса.</span><span class="sxs-lookup"><span data-stu-id="e2623-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="e2623-155">Если  _lpMsgSess_ имеет NULL, сообщение создается независимо от сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2623-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="e2623-156">Если клиентского приложения или поставщика услуг, создав сообщение не освобождает его, а также все его вложения и открытые таблицы, утечка памяти и может привести к завершению приложения.</span><span class="sxs-lookup"><span data-stu-id="e2623-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="e2623-157">MAPI использует функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения и распределения памяти, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e2623-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="e2623-158">Указатели _lpAllocateBuffer,_ _lpAllocateMore_ и _lpFreeBuffer_ являются необязательными, если функция **OpenIMsgOnIStg** вызвана с допустимым параметром _lpMapiSup._</span><span class="sxs-lookup"><span data-stu-id="e2623-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="e2623-159">Так как он имеет дело с объектом OLE, MAPI также должен использовать выделение памяти OLE.</span><span class="sxs-lookup"><span data-stu-id="e2623-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="e2623-160">Дополнительные сведения о структурированных объектах хранения OLE и выделении памяти OLE см. в справочнике _по OLE Programmer._</span><span class="sxs-lookup"><span data-stu-id="e2623-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="e2623-161">Если для _lpMapiSup_ задается действительное значение, **IMessage** поддерживает флаги MAPI_DIALOG и ATTACH_DIALOG путем вызова метода [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) для обеспечения пользовательского интерфейса хода выполнения для методов [IMAPIProp::CopyTo](imapiprop-copyto.md) и [IMessage::D eleteAttach.](imessage-deleteattach.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="e2623-162">Кроме того, метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) пытается преобразовать краткосрочные идентификаторы записей в долгосрочные идентификаторы записей, вызывая метод [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) и вызывая итоговый объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e2623-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="e2623-163">Если для  _lpMapiSup_ передается NULL, **IMessage** игнорирует MAPI_DIALOG и ATTACH_DIALOG и сохраняет краткосрочные идентификаторы записей без преобразования.</span><span class="sxs-lookup"><span data-stu-id="e2623-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="e2623-164">Объект **IStorage,** на который указывает параметр  _lpStg,_ должен быть открыт в режиме STGM_READ или STGM_READWRITE режиме.</span><span class="sxs-lookup"><span data-stu-id="e2623-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="e2623-165">Если используется STGM_READWRITE, необходимо также STGM_TRANSACTED режиме.</span><span class="sxs-lookup"><span data-stu-id="e2623-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="e2623-166">Функция callback, на которая указывает параметр _lpfMsgCallRelease,_ является необязательной; Если он предоставлен, он должен быть основан на прототипе функции [MSGCALLRELEASE.](msgcallrelease.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="e2623-167">Интерфейс **IMessage** вызывает его, когда для отсчета объекта **IMessage**-on-IStorage задается нулевое значение при последнем вызове метода **Release.** </span><span class="sxs-lookup"><span data-stu-id="e2623-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="e2623-168">Функция callback обычно используется для освободить интерфейс **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="e2623-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="e2623-169">**IMessage** не будет пытаться получить доступ к объекту **IStorage,** на который указывает параметр  _lpStg_ после вызова.</span><span class="sxs-lookup"><span data-stu-id="e2623-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="e2623-170">Некоторые клиенты или поставщики могут записывать дополнительные данные в объект **IStorage** помимо записи **IMessage** при его методе [SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="e2623-171">Клиент или поставщик может использовать флаг IMSG_NO_ISTG_COMMIT, чтобы запретить **IMessage** вызывать метод OLE **IStorage::Commit** при обработке вызова **SaveChanges;** в этом случае клиент или поставщик должен сам зафиксировать **объект IStorage** при написании дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="e2623-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="e2623-172">Для этого реализация **IMessage** гарантирует, что все подкатеголи, которые она создает в объекте **IStorage,** начинаются со строки "__", то есть с двумя подчеркиваниями.</span><span class="sxs-lookup"><span data-stu-id="e2623-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="e2623-173">Клиент или поставщик могут избежать конфликтующих имен, не выходя из этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e2623-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="e2623-174">MAPI не определяет поведение нескольких операций открытия, выполняемой в подобекте сообщения, например вложения, потока или внедренного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2623-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="e2623-175">MapI в настоящее время позволяет открыть подобект, который уже открыт, еще раз, но MAPI выполняет операцию открытия, повысив количество ссылок для существующего открытого объекта и вернув его клиенту или поставщику, который вызвал [метод IMessage::OpenAttach](imessage-openattach.md) или [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="e2623-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="e2623-176">Это означает, что для первой операции открытия в подобъекте запрашивается доступ, предоставляемый для всех последующих операций открытия, независимо от доступа, запрашиваемого операциями.</span><span class="sxs-lookup"><span data-stu-id="e2623-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="e2623-177">Правильная процедура размещения сообщения во вложении заключается в вызове метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором интерфейса IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="e2623-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="e2623-178">**В настоящее время OpenProperty** также поддерживает создание вложений сообщений, доступных непосредственно в интерфейсе OLE **IStorage,** то есть с помощью идентификатора IID_IStorage интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e2623-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="e2623-179">**Доступ IStorage** поддерживается, чтобы обеспечить простой способ поместить документ Microsoft Word во вложение без его преобразования в интерфейс OLE **IStream** или из него.</span><span class="sxs-lookup"><span data-stu-id="e2623-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="e2623-180">Однако **IMessage** может вести себя предсказуемо, если **OpenIMsgOnIStg** передает указатель **IStorage** на данные вложения, а затем объекты отпущены в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="e2623-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e2623-181">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e2623-181">MFCMAPI reference</span></span>

<span data-ttu-id="e2623-182">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e2623-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e2623-183">**Файл**</span><span class="sxs-lookup"><span data-stu-id="e2623-183">**File**</span></span>|<span data-ttu-id="e2623-184">**Функция**</span><span class="sxs-lookup"><span data-stu-id="e2623-184">**Function**</span></span>|<span data-ttu-id="e2623-185">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="e2623-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2623-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="e2623-186">File.cpp</span></span>  <br/> |<span data-ttu-id="e2623-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="e2623-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="e2623-188">MFCMAPI использует метод **OpenIMsgOnIStg** для открытия интерфейса IMessage поверх . MSG-файл для обработки файла с помощью MAPI.</span><span class="sxs-lookup"><span data-stu-id="e2623-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2623-189">См. также</span><span class="sxs-lookup"><span data-stu-id="e2623-189">See also</span></span>

- [<span data-ttu-id="e2623-190">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e2623-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

