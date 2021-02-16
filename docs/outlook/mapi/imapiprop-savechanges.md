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
# <a name="imapipropsavechanges"></a><span data-ttu-id="e8882-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e8882-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="e8882-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8882-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8882-105">Вносит постоянные изменения, внесенные в объект с момента последней операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="e8882-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e8882-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8882-106">Parameters</span></span>

 <span data-ttu-id="e8882-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8882-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e8882-108">[in] Битоваяmas флагов, которая управляет тем, что происходит с объектом при методе **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="e8882-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="e8882-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e8882-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="e8882-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="e8882-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="e8882-111">Указывает, что сообщение не было доставлено из Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e8882-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="e8882-112">Этот флаг следует использовать в сочетании с методом [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) и флагом ITEMPROC_FORCE, чтобы указать PST- хранилище, что сообщение имеет право на обработку правил, прежде чем хранилище файлов личных папок (PST) извещение любого клиента прослушивания о том, что сообщение поступило.</span><span class="sxs-lookup"><span data-stu-id="e8882-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="e8882-113">Эти правила применяются только к новым сообщениям, созданным с помощью [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) на сервере, который не является Exchange Server, в этом случае Exchange Server уже обработал бы правила для сообщения.</span><span class="sxs-lookup"><span data-stu-id="e8882-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="e8882-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="e8882-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="e8882-115">Изменения следует вносить в объект, переопределяя предыдущие изменения, внесенные в объект, и объект должен быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="e8882-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="e8882-116">Чтобы операция была успешной, необходимо установить разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="e8882-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="e8882-117">Флаг FORCE_SAVE используется после предыдущего вызова **SaveChanges,** возвращенного MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="e8882-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="e8882-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="e8882-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="e8882-119">Изменения должны быть зафиксированы, а объект должен быть открыт для чтения.</span><span class="sxs-lookup"><span data-stu-id="e8882-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="e8882-120">Дополнительные изменения не вносяся.</span><span class="sxs-lookup"><span data-stu-id="e8882-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="e8882-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="e8882-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="e8882-122">Изменения должны быть зафиксированы, а объект должен быть открыт для разрешения на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="e8882-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="e8882-123">Этот флаг обычно устанавливается, когда объект был впервые открыт для разрешения на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="e8882-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="e8882-124">Последующие изменения объекта разрешены.</span><span class="sxs-lookup"><span data-stu-id="e8882-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="e8882-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e8882-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e8882-126">Позволяет **saveChanges** успешно возвращаться, возможно, до полного охранения изменений.</span><span class="sxs-lookup"><span data-stu-id="e8882-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="e8882-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="e8882-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="e8882-128">Включает фильтрацию нежелательной почты для сохраненного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e8882-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="e8882-129">Поддержка фильтрации нежелательной почты доступна только в том случае, если тип адреса электронной почты отправителя соответствует протоколу SMTP, а сообщение сохранено в хранилище для файлов личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="e8882-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8882-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8882-130">Return value</span></span>

<span data-ttu-id="e8882-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8882-131">S_OK</span></span> 
  
> <span data-ttu-id="e8882-132">Успешное выполнение изменений.</span><span class="sxs-lookup"><span data-stu-id="e8882-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="e8882-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e8882-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e8882-134">**SaveChanges** не может оставить объект открытым для разрешения только для чтения, если KEEP_OPEN_READONLY или разрешение на чтение и записи, если KEEP_OPEN_READWRITE установлен.</span><span class="sxs-lookup"><span data-stu-id="e8882-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="e8882-135">Изменения не вносяся.</span><span class="sxs-lookup"><span data-stu-id="e8882-135">No changes are committed.</span></span> 
    
<span data-ttu-id="e8882-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="e8882-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="e8882-137">Объект изменился с момента открытия.</span><span class="sxs-lookup"><span data-stu-id="e8882-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="e8882-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="e8882-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="e8882-139">Объект был удален с момента его открытия.</span><span class="sxs-lookup"><span data-stu-id="e8882-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8882-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8882-140">Remarks</span></span>

<span data-ttu-id="e8882-141">Метод **IMAPIProp::SaveChanges** делает изменения свойств постоянными для объектов, которые поддерживают модель транзакций обработки, таких как сообщения, вложения, контейнеры адресной книги и объекты пользователей обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e8882-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="e8882-142">Объекты, которые не поддерживают транзакции, такие как папки, хранилища сообщений и разделы профилей, немедленно внося изменения.</span><span class="sxs-lookup"><span data-stu-id="e8882-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="e8882-143">Вызов **SaveChanges** не требуется.</span><span class="sxs-lookup"><span data-stu-id="e8882-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="e8882-144">Так как поставщики служб не должны создавать идентификатор записи для своих объектов, пока не будут сохранены все свойства, свойство **PR_ENTRYID** объекта [(PidTagEntryId)](pidtagentryid-canonical-property.md)может быть доступно только после того, как будет вызван метод **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="e8882-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="e8882-145">Некоторые поставщики ждут, пока KEEP_OPEN_READONLY флага для вызова **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="e8882-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="e8882-146">KEEP_OPEN_READONLY указывает, что изменения, которые будут сохранены в текущем вызове, будут последними изменениями, которые будут внесены в объект.</span><span class="sxs-lookup"><span data-stu-id="e8882-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="e8882-147">В некоторых реализациях реализации в хранилище сообщений новые сообщения не будут отображены в папке, пока клиент не сохранит изменения сообщений с помощью **SaveChanges** и не освободит объекты сообщений с помощью метода [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8882-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="e8882-148">Кроме того, некоторые реализации объектов не могут создавать свойство **PR_ENTRYID** для созданного объекта до тех пор, пока не будет вызван **метод SaveChanges,** а другие могут сделать это только после того, как метод **SaveChanges** будет вызван с помощью KEEP_OPEN_READONLY, задав его в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e8882-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e8882-149">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="e8882-149">Notes to implementers</span></span>

<span data-ttu-id="e8882-150">Если вы получили KEEP_OPEN_READONLY, вы можете оставить доступ к объекту как для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e8882-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="e8882-151">Однако поставщик никогда не может оставлять объект в состоянии "только чтение" при KEEP_OPEN_READWRITE флага.</span><span class="sxs-lookup"><span data-stu-id="e8882-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="e8882-152">Когда клиент сохраняет несколько вложений в нескольких сообщениях, он вызывает метод **SaveChanges** для каждого вложения и каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="e8882-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="e8882-153">Часто клиенты MAPI_DEFERRED_ERRORS для каждого из этих вызовов, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="e8882-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="e8882-154">Вы можете возвращать ошибки при последнем или более ранних вызовах.</span><span class="sxs-lookup"><span data-stu-id="e8882-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="e8882-155">Вы даже можете игнорировать флаг.</span><span class="sxs-lookup"><span data-stu-id="e8882-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="e8882-156">Если KEEP_OPEN_READWRITE или KEEP_OPEN_READONLY вместе с MAPI_DEFERRED_ERRORS, запрос на отсрочку ошибки можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="e8882-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="e8882-157">Если MAPI_DEFERRED_ERRORS в  _ulFlags_ не установлен, для вызова **SaveChanges** может быть возвращена одна из ранее отложенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="e8882-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="e8882-158">Является ли удаленный поставщик транспорта функциональной реализацией этого метода, является необязательным и зависит от других вариантов проектирования в реализации.</span><span class="sxs-lookup"><span data-stu-id="e8882-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="e8882-159">Если вы реализуете этот метод, сделайте это в соответствии с документацией здесь.</span><span class="sxs-lookup"><span data-stu-id="e8882-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="e8882-160">Поскольку объекты папок и объекты состояния не работают, реализация **SaveChanges** удаленным поставщиком транспорта должна возвращать как минимум S_OK без выполнения каких-либо работ.</span><span class="sxs-lookup"><span data-stu-id="e8882-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e8882-161">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e8882-161">Notes to callers</span></span>

<span data-ttu-id="e8882-162">Если клиент передает KEEP_OPEN_READONLY, вызывает метод [IMAPIProp::SetProps,](imapiprop-setprops.md) а затем снова вызывает **SaveChanges,** такая же реализация может привести к сбойу.</span><span class="sxs-lookup"><span data-stu-id="e8882-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="e8882-163">После получения MAPI_E_NO_ACCESS вызова, в котором вы KEEP_OPEN_READWRITE, у вас по-прежнему будет разрешение на чтение и записи объекта.</span><span class="sxs-lookup"><span data-stu-id="e8882-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="e8882-164">Можно вызвать **SaveChanges** еще раз, передав флаг KEEP_OPEN_READONLY или без флагов с KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="e8882-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="e8882-165">То, поддерживает ли поставщик флаг KEEP_OPEN_READWRITE, зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="e8882-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="e8882-166">Чтобы указать, что единственный вызов, который будет выполнен для объекта после **SaveChanges—** **IUnknown::Release,** установите флаги для параметра _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e8882-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e8882-167">Ошибка **saveChanges** указывает, что не удалось сделать ожидающих изменений постоянными.</span><span class="sxs-lookup"><span data-stu-id="e8882-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="e8882-168">Разные поставщики по-разному обрабатывают отсутствие флагов в вызове **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="e8882-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="e8882-169">Некоторые поставщики обрабатывают это состояние так же, как KEEP_OPEN_READONLY; другие поставщики интерпретируют его так же, как KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="e8882-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="e8882-170">По-прежнему другие поставщики отключают объект, если не получают флаги при вызове **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="e8882-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="e8882-171">Некоторые свойства, как правило, вычисляемых свойств, не могут быть обработаны до вызова **SaveChanges** и, в некоторых случаях, **Release**.</span><span class="sxs-lookup"><span data-stu-id="e8882-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="e8882-172">При внесении массовых изменений, таких как сохранение вложений в несколько сообщений, откладывает обработку ошибок, устанавливая флаг MAPI_DEFERRED_ERRORS в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e8882-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="e8882-173">Если вы сохраняете несколько вложений в нескольких сообщениях, сделайте один вызов **SaveChanges** для каждого вложения и один вызов **SaveChanges** для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="e8882-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="e8882-174">Установите флаг MAPI_DEFERRED_ERRORS для каждого вызова вложения и для всех сообщений, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="e8882-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="e8882-175">Если **SaveChanges** возвращает MAPI_E_OBJECT_CHANGED, проверьте, был ли изменен исходный объект.</span><span class="sxs-lookup"><span data-stu-id="e8882-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="e8882-176">В этом случае предупредите пользователя, который может запросить переоценку предыдущих изменений или сохранить объект в другом месте.</span><span class="sxs-lookup"><span data-stu-id="e8882-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="e8882-177">Если исходный объект был удален, предупредить пользователя, чтобы он получил возможность сохранить объект в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="e8882-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="e8882-178">Нельзя вызвать **SaveChanges** с флагом FORCE_SAVE открытого объекта, который был удален.</span><span class="sxs-lookup"><span data-stu-id="e8882-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="e8882-179">Если **SaveChanges** возвращает ошибку, объект, изменения которого нужно сохранить, остается открытым независимо от флагов, установленных в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e8882-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e8882-180">Файлы  _ulFlags_ NON_EMS_XP_SAVE и SPAMFILTER_ONSAVE могут не быть определены в загружаемом файле заголовок, который у вас есть в настоящее время. В этом случае вы можете добавить его в код, используя следующие значения: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="e8882-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="e8882-181">Дополнительные сведения [см. в поддоме "Сохранение свойств MAPI".](saving-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="e8882-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8882-182">См. также</span><span class="sxs-lookup"><span data-stu-id="e8882-182">See also</span></span>



[<span data-ttu-id="e8882-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="e8882-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="e8882-184">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="e8882-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="e8882-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8882-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="e8882-186">Сохранение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="e8882-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

