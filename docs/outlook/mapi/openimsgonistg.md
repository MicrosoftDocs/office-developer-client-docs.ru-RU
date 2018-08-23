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
ms.openlocfilehash: 56e663ced33da933b4276911b609f2fae1c5d78e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563969"
---
# <a name="openimsgonistg"></a><span data-ttu-id="1d403-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="1d403-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="1d403-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d403-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d403-105">Создает новый объект [IMessage](imessageimapiprop.md) поверх существующего объекта OLE **IStorage** , для использования в рамках сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="1d403-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d403-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1d403-106">Header file:</span></span>  <br/> |<span data-ttu-id="1d403-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="1d403-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="1d403-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="1d403-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1d403-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1d403-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1d403-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="1d403-110">Called by:</span></span>  <br/> |<span data-ttu-id="1d403-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="1d403-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1d403-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d403-112">Parameters</span></span>

<span data-ttu-id="1d403-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="1d403-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="1d403-114">[in] Указатель на объект сеанса сообщения, в котором должен быть создан новый **IMessage** **IStorage** объект - on.</span><span class="sxs-lookup"><span data-stu-id="1d403-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="1d403-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="1d403-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="1d403-116">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="1d403-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="1d403-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="1d403-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="1d403-118">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="1d403-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="1d403-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="1d403-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="1d403-120">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="1d403-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="1d403-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="1d403-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="1d403-122">[in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="1d403-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="1d403-123">Интерфейс **IMessage** должен использовать этот метод для распределения при работе с интерфейсами, такие как **IStorage** и **IStream**.</span><span class="sxs-lookup"><span data-stu-id="1d403-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="1d403-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="1d403-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="1d403-125">[in] Необязательный указатель на объект поддержки MAPI, поставщик службы можно использовать для вызова методов [IMAPISupport: IUnknown](imapisupportiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1d403-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="1d403-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="1d403-126">_lpStg_</span></span>
  
> <span data-ttu-id="1d403-127">[in, out] Указатель на объект OLE **IStorage** открытой и только для чтения или разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1d403-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="1d403-128">Так как **IMessage** не поддерживает доступ только для записи, **OpenIMsgOnIStg** не принимает объект хранилища, открытых в режиме только для записи.</span><span class="sxs-lookup"><span data-stu-id="1d403-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="1d403-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="1d403-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="1d403-130">[in] Необязательный указатель на функцию обратного вызова на основании прототип [MSGCALLRELEASE](msgcallrelease.md) , MAPI для вызова после последнего выпуска **IMessage**- on - **IStorage** объекта.</span><span class="sxs-lookup"><span data-stu-id="1d403-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="1d403-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="1d403-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="1d403-132">[in] Данные вызывающего раз сохранена с MAPI с объектом **IStorage** **IMessage**- on - и передается **MSGCALLRELEASE** на основе функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="1d403-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="1d403-133">Данные предоставляет контекст об объекте **IMessage** освобождения и объект **IStorage** , на котором он был создан.</span><span class="sxs-lookup"><span data-stu-id="1d403-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="1d403-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d403-134">_ulFlags_</span></span>
  
> <span data-ttu-id="1d403-135">[in] Битовая маска флаги определять, когда клиентское приложение или поставщик услуг вызывает метод **IMessage::SaveChanges** вызывается метод OLE **IStorage::Commit** .</span><span class="sxs-lookup"><span data-stu-id="1d403-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="1d403-136">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="1d403-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="1d403-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="1d403-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="1d403-138">Метод OLE **IStorage::Commit** — не будет вызываться, когда клиента или поставщика вызывает [SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="1d403-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="1d403-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d403-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="1d403-140">Позволяет создавать файлы MSG-файл в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="1d403-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="1d403-141">Созданный файл [IMessage](imessageimapiprop.md) показывает STORE_UNICODE_OK в его [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) и поддерживает Юникод свойства.</span><span class="sxs-lookup"><span data-stu-id="1d403-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="1d403-142">Флаг MAPI_UNICODE поддерживается только в этой функции в Outlook 2003 или выше.</span><span class="sxs-lookup"><span data-stu-id="1d403-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="1d403-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="1d403-143">_lppMsg_</span></span>
  
> <span data-ttu-id="1d403-144">[out] Указатель на указатель на объект открыт **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="1d403-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1d403-145">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1d403-145">Return value</span></span>

<span data-ttu-id="1d403-146">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1d403-146">S_OK</span></span> 
  
> <span data-ttu-id="1d403-147">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="1d403-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d403-148">���������</span><span class="sxs-lookup"><span data-stu-id="1d403-148">Remarks</span></span>

<span data-ttu-id="1d403-149">Свойство атрибуты осуществляется только на свойство объекты, то есть, реализация [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1d403-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="1d403-150">Чтобы сделать свойства MAPI на объект структурированного хранилища OLE, обеспечивающая **OpenIMsgOnIStg** [IMessage: IMAPIProp](imessageimapiprop.md) объекта поверх объекта OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="1d403-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="1d403-151">Атрибуты свойств для таких объектов можно задать или изменены с помощью [SetAttribIMsgOnIStg](setattribimsgonistg.md) и получены с [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="1d403-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1d403-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1d403-152">Notes to callers</span></span>

<span data-ttu-id="1d403-153">До вызова **OpenIMsgOnIStg** с [OpenIMsgSession](openimsgsession.md) открывать сообщение сеанса.</span><span class="sxs-lookup"><span data-stu-id="1d403-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="1d403-154">Допустимый _lpMsgSess_ параметра сделать sures, создано новое сообщение в рамках сеанса сообщения, чтобы он закрывается при закрытии сеанса.</span><span class="sxs-lookup"><span data-stu-id="1d403-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="1d403-155">Если _lpMsgSess_ имеет значение NULL, независимо от любого сеанса сообщения создается сообщение.</span><span class="sxs-lookup"><span data-stu-id="1d403-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="1d403-156">Если клиентское приложение или поставщика услуг, создавшего сообщение не освободить его, а также все вложения, откройте таблицы памяти является утечка и может привести к завершению работы приложения.</span><span class="sxs-lookup"><span data-stu-id="1d403-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="1d403-157">Функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти, в частности для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объектной использует MAPI Например, [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="1d403-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="1d403-158">При вызове функции **OpenIMsgOnIStg** с параметром допустимый _lpMapiSup_ указатели _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="1d403-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="1d403-159">Так как иметь дело с базовым объектом OLE, MAPI также необходимо использовать выделения памяти для OLE.</span><span class="sxs-lookup"><span data-stu-id="1d403-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="1d403-160">Дополнительные сведения об объектах СТРУКТУРИРОВАННОГО хранилища и выделение памяти OLE можно _OLE Справочник программиста_.</span><span class="sxs-lookup"><span data-stu-id="1d403-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="1d403-161">Если для _lpMapiSup_допустимое значение указано, **IMessage** поддерживает флаги MAPI_DIALOG и ATTACH_DIALOG путем вызова метода [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) , чтобы предоставить интерфейс пользователя о ходе выполнения для [IMAPIProp::CopyTo](imapiprop-copyto.md) и [IMessage::DeleteAttach](imessage-deleteattach.md) методы.</span><span class="sxs-lookup"><span data-stu-id="1d403-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="1d403-162">Кроме того метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) пытается преобразовать краткосрочных идентификаторы записей для долгосрочного идентификаторы записей путем вызова метода [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) и выполнение вызовов на полученный объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1d403-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="1d403-163">Если передается _lpMapiSup_, **IMessage** игнорирует MAPI_DIALOG и ATTACH_DIALOG и сохраняет краткосрочных идентификаторы записей без преобразования.</span><span class="sxs-lookup"><span data-stu-id="1d403-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="1d403-164">Объект **IStorage** , указанный с помощью параметра _lpStg_ необходимо открыть в режиме STGM_READ или STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="1d403-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="1d403-165">Если используется режим STGM_READWRITE, необходимо также установить режим STGM_TRANSACTED.</span><span class="sxs-lookup"><span data-stu-id="1d403-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="1d403-166">Функция обратного вызова, на который указывает параметр _lpfMsgCallRelease_ является необязательным; Если этот параметр указан, он должен быть основан прототип функции [MSGCALLRELEASE](msgcallrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="1d403-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="1d403-167">Интерфейс **IMessage** она вызывается при счетчик ссылок объекта **IMessage**- on - **IStorage** имеет значение нуль при последнем вызове его метода **выпуска** .</span><span class="sxs-lookup"><span data-stu-id="1d403-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="1d403-168">Если функция обратного вызова обычно используется для освобождения основной интерфейс **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="1d403-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="1d403-169">**IMessage** не пытается получить доступ к **IStorage** объект, указанный в параметре _lpStg_ после внесения обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="1d403-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="1d403-170">Некоторые клиенты или Поставщики может записывать дополнительные данные на объекте **IStorage** за пределы какие **IMessage** самого записывает при вызове метода [SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="1d403-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="1d403-171">Клиента или поставщика можно использовать флаг IMSG_NO_ISTG_COMMIT для предотвращения **IMessage** вызов метода OLE **IStorage::Commit** при обработке вызов **SaveChanges** ; в этом случае клиента или поставщика необходимо самого сохранить объект **IStorage** при записи дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="1d403-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="1d403-172">Для помощи в этой реализации **IMessage** гарантирует одно имя, все substorages, которые он создает в объекте **IStorage** , начинающиеся с «__», то есть с двумя подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="1d403-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="1d403-173">Клиента или поставщика можно избежать конфликтов имен, сохранив его вложенного хранилища имена из этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1d403-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="1d403-174">MAPI не определяет поведение нескольких open операций, выполняемых на вложенные объекты сообщения, такие как вложения, потока или внедренных сообщений.</span><span class="sxs-lookup"><span data-stu-id="1d403-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="1d403-175">MAPI в настоящее время позволяет вложенные объекты, открыть, чтобы открыть еще раз, но MAPI выполняет операции открытия, увеличивающееся счетчик ссылок для существующих open объекта и возврат для клиента или поставщика, который называется [IMessage::OpenAttach ](imessage-openattach.md)или метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1d403-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="1d403-176">Это означает, что запрошенный для первой операции открытия на вложенные объекты доступ доступа, для всех последующих операций открытия, независимо от того, запрошенный операциями доступ.</span><span class="sxs-lookup"><span data-stu-id="1d403-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="1d403-177">Правильный процедуру для помещения сообщения в вложение можно вызвать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатор интерфейса IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="1d403-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="1d403-178">**OpenProperty** в настоящее время поддерживает создание вложений сообщений доступны непосредственно в интерфейсе OLE **IStorage** , то есть, с помощью идентификатора интерфейса IID_IStorage.</span><span class="sxs-lookup"><span data-stu-id="1d403-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="1d403-179">Чтобы разрешить простой способ поместить документ Microsoft Word в вложения без преобразования или из интерфейса OLE **IStream** поддерживается **IStorage** доступ.</span><span class="sxs-lookup"><span data-stu-id="1d403-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="1d403-180">Тем не менее если **OpenIMsgOnIStg** передается указатель **IStorage** данные вложения, а затем выпущен объекты в том порядке **IMessage** может работать предсказуемо.</span><span class="sxs-lookup"><span data-stu-id="1d403-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d403-181">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="1d403-181">MFCMAPI reference</span></span>

<span data-ttu-id="1d403-182">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="1d403-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d403-183">**����**</span><span class="sxs-lookup"><span data-stu-id="1d403-183">**File**</span></span>|<span data-ttu-id="1d403-184">**�������**</span><span class="sxs-lookup"><span data-stu-id="1d403-184">**Function**</span></span>|<span data-ttu-id="1d403-185">**�����������**</span><span class="sxs-lookup"><span data-stu-id="1d403-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d403-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="1d403-186">File.cpp</span></span>  <br/> |<span data-ttu-id="1d403-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="1d403-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="1d403-188">Mfcmapi (en) использует метод **OpenIMsgOnIStg** для открытия интерфейс IMessage поверх. MSG файлов, чтобы файл может управлять с помощью интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d403-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d403-189">См. также</span><span class="sxs-lookup"><span data-stu-id="1d403-189">See also</span></span>

- [<span data-ttu-id="1d403-190">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1d403-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

