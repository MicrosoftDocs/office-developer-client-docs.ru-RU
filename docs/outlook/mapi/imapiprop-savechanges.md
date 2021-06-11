---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316634"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="4a996-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4a996-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="4a996-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a996-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a996-105">Вносит постоянные изменения, внесенные в объект с момента последней операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="4a996-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4a996-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4a996-106">Parameters</span></span>

 <span data-ttu-id="4a996-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4a996-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4a996-108">[in] Битмаски флагов, которые контролируют, что происходит с объектом, когда **называется метод IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="4a996-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="4a996-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4a996-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="4a996-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="4a996-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="4a996-111">Указывает, что сообщение не было доставлено из Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4a996-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="4a996-112">Этот флаг следует использовать в сочетании с методом [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) и флагом ITEMPROC_FORCE, чтобы указать в магазине PST, что сообщение имеет право на обработку правил до того, как хранилище личных папок (PST) сообщает любому прослушиваемому клиенту о том, что сообщение пришло.</span><span class="sxs-lookup"><span data-stu-id="4a996-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="4a996-113">Обработка этих правил применяется только к новым сообщениям, созданным с [помощью IMAPIFolder::CreateMessage](imapifolder-createmessage.md) на сервере, который не является Exchange Server, в этом случае Exchange Server уже обработаны правила сообщения.</span><span class="sxs-lookup"><span data-stu-id="4a996-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="4a996-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="4a996-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="4a996-115">Изменения должны быть записаны в объект, переопределив все предыдущие изменения, внесенные в объект, и объект должен быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="4a996-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="4a996-116">Для успешной операции необходимо задать разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="4a996-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="4a996-117">Флаг FORCE_SAVE используется после предыдущего вызова **в SaveChanges,** возвращенного MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="4a996-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="4a996-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="4a996-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="4a996-119">Необходимо внести изменения, а объект должен быть открыт для чтения.</span><span class="sxs-lookup"><span data-stu-id="4a996-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="4a996-120">Дополнительные изменения не будут внесены.</span><span class="sxs-lookup"><span data-stu-id="4a996-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="4a996-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="4a996-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="4a996-122">Необходимо внести изменения, а объект должен быть открыт для разрешения на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="4a996-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="4a996-123">Этот флаг обычно устанавливается, когда объект был впервые открыт для разрешения на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="4a996-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="4a996-124">Допускаются последующие изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="4a996-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="4a996-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4a996-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4a996-126">Позволяет **saveChanges** успешно возвращаться, возможно, до полного совершения изменений.</span><span class="sxs-lookup"><span data-stu-id="4a996-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="4a996-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="4a996-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="4a996-128">Включает фильтрацию нежелательной почты на сохраненное сообщение.</span><span class="sxs-lookup"><span data-stu-id="4a996-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="4a996-129">Поддержка фильтрации нежелательной почты доступна только в том случае, если тип адреса электронной почты отправителя соответствует протоколу SMTP, а сообщение сохранено в хранилище для файлов личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="4a996-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a996-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a996-130">Return value</span></span>

<span data-ttu-id="4a996-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a996-131">S_OK</span></span> 
  
> <span data-ttu-id="4a996-132">Выполнение изменений было успешным.</span><span class="sxs-lookup"><span data-stu-id="4a996-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="4a996-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4a996-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4a996-134">**SaveChanges** не может сохранить объект открытым для разрешения только для чтения, если KEEP_OPEN_READONLY установлено, или разрешения на чтение и записи, если KEEP_OPEN_READWRITE задарен.</span><span class="sxs-lookup"><span data-stu-id="4a996-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="4a996-135">Изменения не внося.</span><span class="sxs-lookup"><span data-stu-id="4a996-135">No changes are committed.</span></span> 
    
<span data-ttu-id="4a996-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="4a996-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="4a996-137">Объект изменился с момента его открытия.</span><span class="sxs-lookup"><span data-stu-id="4a996-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="4a996-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="4a996-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="4a996-139">Объект был удален с момента его открытия.</span><span class="sxs-lookup"><span data-stu-id="4a996-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a996-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a996-140">Remarks</span></span>

<span data-ttu-id="4a996-141">Метод **IMAPIProp::SaveChanges** делает изменения свойств постоянными для объектов, поддерживаюющих модель обработки транзакций, таких как сообщения, вложения, контейнеры адресных книг и объекты пользователей обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4a996-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="4a996-142">Объекты, которые не поддерживают транзакции, такие как папки, хранилища сообщений и разделы профилей, немедленно внося изменения.</span><span class="sxs-lookup"><span data-stu-id="4a996-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="4a996-143">Вызов в **SaveChanges** не требуется.</span><span class="sxs-lookup"><span data-stu-id="4a996-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="4a996-144">Так как поставщики служб не должны создавать идентификатор входа для своих объектов до тех пор, пока не будут сохранены все свойства, свойство **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)может быть доступно только после того, как будет вызван метод **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="4a996-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="4a996-145">Некоторые поставщики ждут, пока флаг KEEP_OPEN_READONLY на **вызове SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="4a996-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="4a996-146">KEEP_OPEN_READONLY указывает, что изменения, которые будут сохранены в текущем вызове, будут последними изменениями, которые будут внесены на объекте.</span><span class="sxs-lookup"><span data-stu-id="4a996-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="4a996-147">Некоторые реализации магазина сообщений не показывают вновь созданные сообщения в папке, пока клиент не сохранит изменения сообщений с помощью **SaveChanges** и не выпустит объекты сообщений с помощью метода [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a996-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="4a996-148">Кроме того, некоторые объектные **реализации** не могут создавать свойство PR_ENTRYID для вновь созданного объекта до тех пор, пока не будут вызваны **SaveChanges,** а некоторые могут сделать это только после того, как **saveChanges** был вызван с помощью KEEP_OPEN_READONLY, задатого в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="4a996-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4a996-149">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="4a996-149">Notes to implementers</span></span>

<span data-ttu-id="4a996-150">Если вы получаете флаг KEEP_OPEN_READONLY, у вас есть возможность оставить доступ объекта в качестве чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="4a996-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="4a996-151">Однако поставщик никогда не может оставить объект в состоянии только для чтения при KEEP_OPEN_READWRITE флага.</span><span class="sxs-lookup"><span data-stu-id="4a996-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="4a996-152">Когда клиент сохраняет несколько вложений для нескольких сообщений, он вызывает метод **SaveChanges** для каждого вложения и каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4a996-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="4a996-153">Часто клиенты MAPI_DEFERRED_ERRORS для каждого из этих вызовов, за исключением последнего.</span><span class="sxs-lookup"><span data-stu-id="4a996-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="4a996-154">Ошибки можно возвращать с помощью последнего звонка или более ранних вызовов.</span><span class="sxs-lookup"><span data-stu-id="4a996-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="4a996-155">Вы даже можете игнорировать флаг.</span><span class="sxs-lookup"><span data-stu-id="4a996-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="4a996-156">Если KEEP_OPEN_READWRITE или KEEP_OPEN_READONLY установлен вместе с MAPI_DEFERRED_ERRORS, можно игнорировать запрос на отсрочку ошибки.</span><span class="sxs-lookup"><span data-stu-id="4a996-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="4a996-157">Если MAPI_DEFERRED_ERRORS в _ulFlags_ не установлено, одна из ранее отложенных ошибок может быть возвращена для вызова **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="4a996-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="4a996-158">Предоставляет ли удаленный поставщик транспорта функциональную реализацию этого метода необязательным и зависит от других вариантов проектирования в реализации.</span><span class="sxs-lookup"><span data-stu-id="4a996-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="4a996-159">Если вы реализуете этот метод, сделайте это в соответствии с документацией здесь.</span><span class="sxs-lookup"><span data-stu-id="4a996-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="4a996-160">Так как объекты папок и объекты состояния не трансактироваться, как минимум, реализация **saveChanges** удаленного поставщика транспорта должна возвращаться S_OK без выполнения каких-либо работ.</span><span class="sxs-lookup"><span data-stu-id="4a996-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4a996-161">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4a996-161">Notes to callers</span></span>

<span data-ttu-id="4a996-162">Если клиент проходит KEEP_OPEN_READONLY, вызывает [метод IMAPIProp::SetProps](imapiprop-setprops.md) и снова вызывает **SaveChanges,** такая же реализация может привести к сбой.</span><span class="sxs-lookup"><span data-stu-id="4a996-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="4a996-163">После получения MAPI_E_NO_ACCESS звонка, в котором KEEP_OPEN_READWRITE, вы будете продолжать получать разрешение на чтение и записи объекта.</span><span class="sxs-lookup"><span data-stu-id="4a996-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="4a996-164">Вы можете вызвать **SaveChanges** снова, передав флаг KEEP_OPEN_READONLY или без флагов с KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="4a996-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="4a996-165">Поддерживает ли поставщик флаг KEEP_OPEN_READWRITE зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="4a996-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="4a996-166">Чтобы указать, что единственный вызов, который будет выполнен на объекте после **SaveChanges,** это **IUnknown::Release,** не установите флаги для _параметра ulFlags._</span><span class="sxs-lookup"><span data-stu-id="4a996-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="4a996-167">Ошибка, **допущенная в SaveChanges,** указывает на то, что она не может сделать ожидающих изменений постоянными.</span><span class="sxs-lookup"><span data-stu-id="4a996-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="4a996-168">Различные поставщики по-разному обрабатывают отсутствие флагов в **вызове SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="4a996-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="4a996-169">Некоторые поставщики обрабатывают это состояние так же, как KEEP_OPEN_READONLY; другие поставщики интерпретируют его так же, как KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="4a996-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="4a996-170">Однако другие поставщики закрывают объект, если они не получают флаги при вызове **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="4a996-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="4a996-171">Некоторые свойства, как правило, вычисляемых свойств, не могут быть обработаны до вызова **SaveChanges** и, в некоторых случаях, **выпуска**.</span><span class="sxs-lookup"><span data-stu-id="4a996-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="4a996-172">При внесении массовых изменений, например сохранения вложений в несколько сообщений, откладывать обработку ошибок, установив флаг MAPI_DEFERRED_ERRORS  _в ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="4a996-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="4a996-173">Если вы сохраните несколько вложений для нескольких сообщений, сделайте один вызов **SaveChanges** для каждого вложения и один **вызов SaveChanges** для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4a996-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="4a996-174">Установите флаг MAPI_DEFERRED_ERRORS для каждого вызова вложения и для всех сообщений, за исключением последнего.</span><span class="sxs-lookup"><span data-stu-id="4a996-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="4a996-175">Если **SaveChanges** возвращает MAPI_E_OBJECT_CHANGED, проверьте, был ли изменен исходный объект.</span><span class="sxs-lookup"><span data-stu-id="4a996-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="4a996-176">Если да, предупредите пользователя, который может запросить переоценку предыдущих изменений или сохранить объект в другом месте.</span><span class="sxs-lookup"><span data-stu-id="4a996-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="4a996-177">Если исходный объект удален, предупредить пользователя предоставить ему возможность сохранить объект в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="4a996-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="4a996-178">Нельзя вызывать **SaveChanges** с FORCE_SAVE флагом на открытом объекте, который был удален.</span><span class="sxs-lookup"><span data-stu-id="4a996-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="4a996-179">Если **SaveChanges** возвращает ошибку, объект, изменения которого должны были быть сохранены, остается открытым независимо от флагов, заданных в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="4a996-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4a996-180">_UlFlags_ NON_EMS_XP_SAVE и SPAMFILTER_ONSAVE не могут быть определены в загружаемом файле заголовки, который у вас есть в настоящее время, и в этом случае вы можете добавить его в код с помощью следующих значений: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="4a996-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="4a996-181">Дополнительные сведения см. в [дополнительных сведениях о сохранении свойств MAPI.](saving-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="4a996-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a996-182">См. также</span><span class="sxs-lookup"><span data-stu-id="4a996-182">See also</span></span>



[<span data-ttu-id="4a996-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="4a996-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="4a996-184">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="4a996-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="4a996-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a996-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="4a996-186">Сохранение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="4a996-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

