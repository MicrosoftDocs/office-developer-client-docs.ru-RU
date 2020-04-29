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
# <a name="openimsgonistg"></a><span data-ttu-id="87b9f-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="87b9f-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="87b9f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87b9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87b9f-105">Создает новый объект [iMessage](imessageimapiprop.md) поверх существующего объекта OLE **IStorage** , который будет использоваться в сеансе сообщений.</span><span class="sxs-lookup"><span data-stu-id="87b9f-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87b9f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="87b9f-106">Header file:</span></span>  <br/> |<span data-ttu-id="87b9f-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="87b9f-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="87b9f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="87b9f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="87b9f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="87b9f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="87b9f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="87b9f-110">Called by:</span></span>  <br/> |<span data-ttu-id="87b9f-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="87b9f-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="87b9f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="87b9f-112">Parameters</span></span>

<span data-ttu-id="87b9f-113">_лпмсгсесс_</span><span class="sxs-lookup"><span data-stu-id="87b9f-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="87b9f-114">возврата Указатель на объект сеанса сообщения, в котором будет создан новый объект **iMessage**-On- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="87b9f-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="87b9f-115">_лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="87b9f-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="87b9f-116">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="87b9f-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="87b9f-117">_лпаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="87b9f-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="87b9f-118">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="87b9f-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="87b9f-119">_лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="87b9f-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="87b9f-120">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="87b9f-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="87b9f-121">_лпмаллок_</span><span class="sxs-lookup"><span data-stu-id="87b9f-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="87b9f-122">возврата Указатель на объект распределителя памяти, который предоставляет интерфейс для **выделения** OLE.</span><span class="sxs-lookup"><span data-stu-id="87b9f-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="87b9f-123">Интерфейс **iMessage** должен использовать этот метод распределения при работе с такими интерфейсами, как **IStorage** и **IStream**.</span><span class="sxs-lookup"><span data-stu-id="87b9f-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="87b9f-124">_лпмаписуп_</span><span class="sxs-lookup"><span data-stu-id="87b9f-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="87b9f-125">возврата Необязательный указатель на объект поддержки MAPI, который поставщик услуг может использовать для вызова методов интерфейса [имаписуппорт: IUnknown](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="87b9f-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="87b9f-126">_лпстг_</span><span class="sxs-lookup"><span data-stu-id="87b9f-126">_lpStg_</span></span>
  
> <span data-ttu-id="87b9f-127">[вход, выход] Указатель на объект OLE **IStorage** , который открыт и имеет разрешение только на чтение или чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="87b9f-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="87b9f-128">Так как **iMessage** не поддерживает доступ только для записи, **опенимсгонистг** не принимает объект хранилища, Открытый в режиме "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="87b9f-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="87b9f-129">_лпфмсгкаллрелеасе_</span><span class="sxs-lookup"><span data-stu-id="87b9f-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="87b9f-130">возврата Необязательный указатель на функцию обратного вызова, основанный на прототипе [мсгкаллрелеасе](msgcallrelease.md) , который вызывается с помощью MAPI после последнего выпуска объекта **iMessage**-On- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="87b9f-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="87b9f-131">_улкаллердата_</span><span class="sxs-lookup"><span data-stu-id="87b9f-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="87b9f-132">возврата Данные вызывающего абонента, сохраненные MAPI с помощью объекта **iMessage**On/ **IStorage** и переданные в функцию обратного вызова на основе **мсгкаллрелеасе** .</span><span class="sxs-lookup"><span data-stu-id="87b9f-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="87b9f-133">Данные предоставляют контекст для вызываемого объекта **iMessage** и объект **IStorage** поверх его построения.</span><span class="sxs-lookup"><span data-stu-id="87b9f-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="87b9f-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87b9f-134">_ulFlags_</span></span>
  
> <span data-ttu-id="87b9f-135">возврата Битовая маска флагов, используемых для управления тем, вызывает ли метод OLE **IStorage:: Commit** , когда клиентское приложение или поставщик услуг вызывает метод **iMessage:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="87b9f-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="87b9f-136">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="87b9f-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="87b9f-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="87b9f-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="87b9f-138">Метод OLE **IStorage:: Commit** не вызывается, когда клиент или поставщик вызывает [SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="87b9f-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="87b9f-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87b9f-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="87b9f-140">Позволяет создавать файлы Unicode. MSG.</span><span class="sxs-lookup"><span data-stu-id="87b9f-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="87b9f-141">Полученный в результате файл [iMessage](imessageimapiprop.md) показывает STORE_UNICODE_OK в [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) и поддерживает свойства Юникода.</span><span class="sxs-lookup"><span data-stu-id="87b9f-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="87b9f-142">Флаг MAPI_UNICODE поддерживается только в этой функции в Outlook 2003 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="87b9f-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="87b9f-143">_лппмсг_</span><span class="sxs-lookup"><span data-stu-id="87b9f-143">_lppMsg_</span></span>
  
> <span data-ttu-id="87b9f-144">вышли Указатель на указатель на открытый объект **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="87b9f-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="87b9f-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87b9f-145">Return value</span></span>

<span data-ttu-id="87b9f-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="87b9f-146">S_OK</span></span> 
  
> <span data-ttu-id="87b9f-147">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="87b9f-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87b9f-148">Примечания</span><span class="sxs-lookup"><span data-stu-id="87b9f-148">Remarks</span></span>

<span data-ttu-id="87b9f-149">Доступ к атрибутам свойств возможен только для объектов Property, то есть объектов, реализующих интерфейс [IMAPIProp: IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="87b9f-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="87b9f-150">Чтобы сделать свойства MAPI доступными в объекте структурированного хранилища OLE, **опенимсгонистг** создает объект [iMessage: IMAPIProp](imessageimapiprop.md) в начале объекта OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="87b9f-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="87b9f-151">Атрибуты свойств таких объектов можно задавать или изменять с помощью [сетаттрибимсгонистг](setattribimsgonistg.md) и извлекаются с помощью [жетаттрибимсгонистг](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="87b9f-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="87b9f-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="87b9f-152">Notes to callers</span></span>

<span data-ttu-id="87b9f-153">Перед вызовом **опенимсгонистг** необходимо открыть сеанс сообщений с [опенимсгсессион](openimsgsession.md) .</span><span class="sxs-lookup"><span data-stu-id="87b9f-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="87b9f-154">Указание допустимого параметра _лпмсгсесс_ гарантирует, что новое сообщение будет создано в сеансе сообщений, чтобы оно закрылось при закрытии сеанса.</span><span class="sxs-lookup"><span data-stu-id="87b9f-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="87b9f-155">Если _лпмсгсесс_ имеет значение null, сообщение создается независимо от любого сеанса сообщения.</span><span class="sxs-lookup"><span data-stu-id="87b9f-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="87b9f-156">Если клиентское приложение или поставщик услуг, создавший сообщение, не освобождает его, а также все его вложения и открытые таблицы, память утечки и может привести к завершению работы приложения.</span><span class="sxs-lookup"><span data-stu-id="87b9f-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="87b9f-157">MAPI использует функции, на которые указывает _лпаллокатебуффер_, _лпаллокатеморе_и _лпфрибуффер_ для большей части памяти и освобождений, в частности, для выделения памяти, используемой клиентскими приложениями при вызове интерфейсов объектов, таких как [IMAPIProp::](imapiprop-getprops.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="87b9f-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="87b9f-158">Указатели _лпаллокатебуффер_, _лпаллокатеморе_и _Лпфрибуффер_ необязательны, если функция **опенимсгонистг** вызывается с допустимым параметром _лпмаписуп_ .</span><span class="sxs-lookup"><span data-stu-id="87b9f-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="87b9f-159">Так как он работает с базовым объектом OLE, для MAPI также необходимо использовать выделение памяти OLE.</span><span class="sxs-lookup"><span data-stu-id="87b9f-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="87b9f-160">Дополнительные сведения об объектах структурированного хранилища OLE и выделении памяти OLE приведены в статье _Справочник программиста по OLE_.</span><span class="sxs-lookup"><span data-stu-id="87b9f-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="87b9f-161">Если для _лпмаписуп_указано допустимое значение, **iMessage** поддерживает флаги MAPI_DIALOG и ATTACH_DIALOG, вызывая метод [имаписуппорт::D опрогрессдиалог](imapisupport-doprogressdialog.md) для предоставления пользовательского интерфейса хода выполнения для методов [IMAPIProp:: CopyTo](imapiprop-copyto.md) и [iMessage::D елетеаттач](imessage-deleteattach.md) .</span><span class="sxs-lookup"><span data-stu-id="87b9f-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="87b9f-162">Кроме того, метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) пытается преобразовать краткосрочные идентификаторы записей в долгосрочные идентификаторы записей, вызвав метод [Имаписуппорт:: опенаддрессбук](imapisupport-openaddressbook.md) и совершая вызовы для полученного объекта адресной книги.</span><span class="sxs-lookup"><span data-stu-id="87b9f-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="87b9f-163">Если для _лпмаписуп_передается значение null, **iMessage** игнорирует MAPI_DIALOG и ATTACH_DIALOG и сохраняет краткосрочные идентификаторы записей без преобразования.</span><span class="sxs-lookup"><span data-stu-id="87b9f-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="87b9f-164">Объект **IStorage** , на который указывает параметр _лпстг_ , должен быть открыт в режиме STGM_READ или STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="87b9f-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="87b9f-165">Если используется режим STGM_READWRITE, также необходимо задать режим STGM_TRANSACTED.</span><span class="sxs-lookup"><span data-stu-id="87b9f-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="87b9f-166">Функция обратного вызова, на которую указывает параметр _лпфмсгкаллрелеасе_ , является необязательной; Если этот параметр указан, он должен основываться на прототипе функции [мсгкаллрелеасе](msgcallrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="87b9f-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="87b9f-167">Интерфейс **iMessage** вызывает его, когда значение счетчика ссылок объекта **iMessage**-On- **IStorage** задается равным нулю по последнему вызову метода **Release** .</span><span class="sxs-lookup"><span data-stu-id="87b9f-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="87b9f-168">Функция обратного вызова обычно используется для освобождения базового интерфейса **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="87b9f-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="87b9f-169">**IMessage** не будет пытаться получить доступ к объекту **IStorage** , на который указывает параметр _лпстг_ после выполнения обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="87b9f-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="87b9f-170">Некоторые клиенты или поставщики могут записывать дополнительные данные в объект **IStorage** , помимо того, что **iMessage** записывает при вызове метода [SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="87b9f-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="87b9f-171">Клиент или поставщик могут использовать флаг IMSG_NO_ISTG_COMMIT, чтобы запретить **iMessage** вызывать метод "OLE **IStorage:: Commit** " при обработке вызова **SaveChanges** ; в этом случае клиент или поставщик должны зафиксировать объект **IStorage** при записи дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="87b9f-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="87b9f-172">Для этого реализация **iMessage** гарантирует именование всех подхранилищ, которые он создает, в объекте **IStorage** , начиная со строки "__", то есть с двумя знаками подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="87b9f-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="87b9f-173">Клиент или поставщик может избежать конфликтов имен, сохраняя их имена из этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="87b9f-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="87b9f-174">MAPI не определяет поведение нескольких операций открытия, выполняемых над вложенным объектом сообщения, например вложением, потоком или внедренным сообщением.</span><span class="sxs-lookup"><span data-stu-id="87b9f-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="87b9f-175">В настоящее время MAPI позволяет открыть еще один подобъект, который уже открыт, но MAPI выполняет операцию открытия путем увеличения числа ссылок для существующего открытого объекта и возвращения его клиенту или поставщику, вызвавшему метод [iMessage:: опенаттач](imessage-openattach.md) или [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="87b9f-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="87b9f-176">Это означает, что доступ, запрошенный для первой операции открытия для подобъекта, является доступным для всех последующих операций открытия, независимо от доступа, запрашиваемого операциями.</span><span class="sxs-lookup"><span data-stu-id="87b9f-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="87b9f-177">Чтобы поместить сообщение в вложение, нужно вызвать метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) с идентификатором интерфейса IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="87b9f-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="87b9f-178">В настоящее время **опенпроперти** также поддерживает создание вложений сообщений, доступных непосредственно в интерфейсе OLE **IStorage** , то есть с помощью идентификатора интерфейса IID_IStorage.</span><span class="sxs-lookup"><span data-stu-id="87b9f-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="87b9f-179">Доступ **IStorage** поддерживается, чтобы обеспечить простой способ поместить документ Microsoft Word во вложение без преобразования его в интерфейс OLE **IStream** или из него.</span><span class="sxs-lookup"><span data-stu-id="87b9f-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="87b9f-180">Однако **iMessage** может вести себя непредсказуемо, если **опенимсгонистг** передается указатель **IStorage** на данные вложения, а затем объекты освобождаются в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="87b9f-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="87b9f-181">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="87b9f-181">MFCMAPI reference</span></span>

<span data-ttu-id="87b9f-182">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="87b9f-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="87b9f-183">**Файл**</span><span class="sxs-lookup"><span data-stu-id="87b9f-183">**File**</span></span>|<span data-ttu-id="87b9f-184">**Функция**</span><span class="sxs-lookup"><span data-stu-id="87b9f-184">**Function**</span></span>|<span data-ttu-id="87b9f-185">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="87b9f-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87b9f-186">Файл. cpp</span><span class="sxs-lookup"><span data-stu-id="87b9f-186">File.cpp</span></span>  <br/> |<span data-ttu-id="87b9f-187">лоадмсгтомессаже</span><span class="sxs-lookup"><span data-stu-id="87b9f-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="87b9f-188">MFCMAPI использует метод **опенимсгонистг** для открытия интерфейса IMessage на основе. MSG, чтобы файл мог управляться с помощью MAPI.</span><span class="sxs-lookup"><span data-stu-id="87b9f-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87b9f-189">См. также</span><span class="sxs-lookup"><span data-stu-id="87b9f-189">See also</span></span>

- [<span data-ttu-id="87b9f-190">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="87b9f-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

