---
title: Имапипропсавечанжес
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
# <a name="imapipropsavechanges"></a><span data-ttu-id="d7257-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d7257-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="d7257-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7257-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7257-105">Делает неизменными все изменения, внесенные в объект с момента последнего выполнения операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="d7257-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d7257-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7257-106">Parameters</span></span>

 <span data-ttu-id="d7257-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7257-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d7257-108">возврата Битовая маска флагов, определяющих, что происходит с объектом при вызове метода **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="d7257-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="d7257-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d7257-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="d7257-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="d7257-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="d7257-111">Указывает, что сообщение не было доставлено с сервера Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="d7257-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="d7257-112">Этот флаг следует использовать в сочетании с методом [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) и флагом итемпрок_форце, чтобы указать, что сообщение доступно для обработки правилами до того, как хранилище файлов личных папок (PST) уведомит прослушивающий клиент, полученный сообщением.</span><span class="sxs-lookup"><span data-stu-id="d7257-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="d7257-113">Эта обработка правил применяется только к новым сообщениям, созданным с помощью [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) на сервере, который не является сервером Exchange Server, в этом случае сервер Exchange уже обработал правила для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7257-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="d7257-114">ФОРЦЕ_САВЕ</span><span class="sxs-lookup"><span data-stu-id="d7257-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="d7257-115">Изменения должны быть записаны в объект, переопределяя все предыдущие изменения, внесенные в объект, и объект должен быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="d7257-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="d7257-116">Для успешного выполнения операции должно быть задано разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="d7257-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="d7257-117">Флаг ФОРЦЕ_САВЕ используется после предыдущего вызова метода **SaveChanges** , возвращаемого мапи_е_обжект_чанжед.</span><span class="sxs-lookup"><span data-stu-id="d7257-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="d7257-118">КИП_ОПЕН_РЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="d7257-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="d7257-119">Изменения должны быть зафиксированы и объект должен оставаться открытым для чтения.</span><span class="sxs-lookup"><span data-stu-id="d7257-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="d7257-120">Дополнительные изменения не выполняются.</span><span class="sxs-lookup"><span data-stu-id="d7257-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="d7257-121">КИП_ОПЕН_РЕАДВРИТЕ</span><span class="sxs-lookup"><span data-stu-id="d7257-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="d7257-122">Изменения должны быть зафиксированы, а объект должен оставаться открытым для разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="d7257-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="d7257-123">Этот флаг обычно устанавливается при первом открытии объекта для разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="d7257-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="d7257-124">Дальнейшие изменения объекта разрешены.</span><span class="sxs-lookup"><span data-stu-id="d7257-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="d7257-125">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="d7257-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d7257-126">Позволяет успешно возвращать **SaveChanges** , возможно, до того, как изменения будут полностью зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="d7257-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="d7257-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="d7257-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="d7257-128">Включает фильтрацию нежелательной почты для сохраняемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7257-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="d7257-129">Поддержка фильтрации нежелательной почты доступна только в том случае, если тип адреса электронной почты отправителя соответствует протоколу SMTP, а сообщение сохранено в хранилище для файлов личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="d7257-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7257-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7257-130">Return value</span></span>

<span data-ttu-id="d7257-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7257-131">S_OK</span></span> 
  
> <span data-ttu-id="d7257-132">Фиксация изменений выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d7257-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="d7257-133">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="d7257-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d7257-134">**SaveChanges** не может оставить объект открытым для разрешения только для чтения, если задано значение кип_опен_реадонли, или разрешение на чтение и запись, если задано значение кип_опен_реадврите.</span><span class="sxs-lookup"><span data-stu-id="d7257-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="d7257-135">Изменения не фиксируются.</span><span class="sxs-lookup"><span data-stu-id="d7257-135">No changes are committed.</span></span> 
    
<span data-ttu-id="d7257-136">МАПИ_Е_ОБЖЕКТ_ЧАНЖЕД</span><span class="sxs-lookup"><span data-stu-id="d7257-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="d7257-137">Объект изменился с момента его открытия.</span><span class="sxs-lookup"><span data-stu-id="d7257-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="d7257-138">МАПИ_Е_ОБЖЕКТ_ДЕЛЕТЕД</span><span class="sxs-lookup"><span data-stu-id="d7257-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="d7257-139">Объект был удален после его открытия.</span><span class="sxs-lookup"><span data-stu-id="d7257-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7257-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7257-140">Remarks</span></span>

<span data-ttu-id="d7257-141">Метод **IMAPIProp:: SaveChanges** вносит изменения свойств в постоянные для объектов, поддерживающих модель обработки транзакций, таких как сообщения, вложения, контейнеры адресной книги и пользовательские объекты обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d7257-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="d7257-142">Объекты, не поддерживающие транзакции, такие как папки, хранилища сообщений и разделы профилей, немедленно выполняют изменения.</span><span class="sxs-lookup"><span data-stu-id="d7257-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="d7257-143">Вызов **SaveChanges** не требуется.</span><span class="sxs-lookup"><span data-stu-id="d7257-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="d7257-144">Так как поставщики услуг не требуют создания идентификатора записи для своих объектов до тех пор, пока все свойства не будут сохранены, свойство объекта **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) может быть недоступно до тех пор, пока не будет выбран метод **SaveChanges** . вызван.</span><span class="sxs-lookup"><span data-stu-id="d7257-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="d7257-145">Некоторые поставщики ожидают, пока не будет установлен флаг КИП_ОПЕН_РЕАДОНЛИ для вызова **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="d7257-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="d7257-146">КИП_ОПЕН_РЕАДОНЛИ указывает, что изменения, сохраняемые в текущем вызове, будут последними изменениями, которые будут выполнены для объекта.</span><span class="sxs-lookup"><span data-stu-id="d7257-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="d7257-147">Некоторые реализации хранилищ сообщений не показывают новые сообщения в папке до тех пор, пока клиент не сохранит изменения в сообщениях с помощью **SaveChanges** и освободит объекты сообщения с помощью метода [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d7257-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="d7257-148">Кроме того, некоторые реализации объектов не могут создавать свойство **пр_ентрид** для только что созданного объекта, пока не будет вызван метод **SaveChanges** , а некоторые из них могут сделать это только после вызова **SaveChanges** с помощью кип_опен_реадонли задается в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="d7257-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d7257-149">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d7257-149">Notes to implementers</span></span>

<span data-ttu-id="d7257-150">Если вы получаете флаг КИП_ОПЕН_РЕАДОНЛИ, вы можете оставить доступ к объекту как для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d7257-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="d7257-151">Однако поставщик не может оставить объект в состоянии "только для чтения", когда передается флаг КИП_ОПЕН_РЕАДВРИТЕ.</span><span class="sxs-lookup"><span data-stu-id="d7257-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="d7257-152">Когда клиент сохраняет несколько вложений в несколько сообщений, он вызывает метод **SaveChanges** для каждого вложения и каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7257-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="d7257-153">Часто клиенты задают МАПИ_ДЕФЕРРЕД_ЕРРОРС для каждого из этих вызовов, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="d7257-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="d7257-154">Ошибки можно возвращать при последнем вызове или более ранних вызовах.</span><span class="sxs-lookup"><span data-stu-id="d7257-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="d7257-155">Вы можете даже проигнорировать флаг.</span><span class="sxs-lookup"><span data-stu-id="d7257-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="d7257-156">Если параметр КИП_ОПЕН_РЕАДВРИТЕ или КИП_ОПЕН_РЕАДОНЛИ задан вместе с МАПИ_ДЕФЕРРЕД_ЕРРОРС, вы можете пропустить запрос ошибки дефермент.</span><span class="sxs-lookup"><span data-stu-id="d7257-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="d7257-157">Если МАПИ_ДЕФЕРРЕД_ЕРРОРС не задан в _ulFlags_, то для вызова **SaveChanges** можно возвратить одну из ранее обнаруженных ошибок.</span><span class="sxs-lookup"><span data-stu-id="d7257-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="d7257-158">Предоставляет ли удаленный поставщик транспорта функциональную реализацию этого метода, это необязательно и зависит от других вариантов дизайна в вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="d7257-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="d7257-159">Если вы реализуете этот метод, сделайте это в соответствии с документацией.</span><span class="sxs-lookup"><span data-stu-id="d7257-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="d7257-160">Так как объекты Folder и Status не являются транзакционными, по крайней мере, реализация **SaveChanges** удаленным поставщиком транспорта должна возВРАЩАТЬ значение S_OK без фактического выполнения каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="d7257-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d7257-161">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d7257-161">Notes to callers</span></span>

<span data-ttu-id="d7257-162">Если клиент передает КИП_ОПЕН_РЕАДОНЛИ, вызывает метод [IMAPIProp:: SetProps](imapiprop-setprops.md) , а затем снова вызывает **SaveChanges** , та же реализация может закончиться с ошибками.</span><span class="sxs-lookup"><span data-stu-id="d7257-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="d7257-163">После получения МАПИ_Е_НО_АКЦЕСС из вызова, в котором вы задаете КИП_ОПЕН_РЕАДВРИТЕ, у вас остается разрешение на чтение и запись для объекта.</span><span class="sxs-lookup"><span data-stu-id="d7257-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="d7257-164">Вы можете вызвать метод **SaveChanges** еще раз, ПЕРЕДАВ флаг кип_опен_реадонли или без флагов с кип_опен_суффикс.</span><span class="sxs-lookup"><span data-stu-id="d7257-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="d7257-165">Поддерживает ли поставщик флаг КИП_ОПЕН_РЕАДВРИТЕ, зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="d7257-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="d7257-166">Чтобы указать, что единственный вызов, который следует выполнить для объекта, после **SaveChanges** — **IUnknown:: Release**, set без флагов для параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d7257-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d7257-167">Сообщение об ошибке **SaveChanges** указывает на то, что не удалось сделать ожидающие изменения постоянными.</span><span class="sxs-lookup"><span data-stu-id="d7257-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="d7257-168">Различные поставщики обрабатывают отсутствие флагов для вызова **SaveChanges** по-разному.</span><span class="sxs-lookup"><span data-stu-id="d7257-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="d7257-169">Некоторые поставщики считают это состояние тем же, что и КИП_ОПЕН_РЕАДОНЛИ; другие поставщики интерпретируют его так же, как КИП_ОПЕН_РЕАДВРИТЕ.</span><span class="sxs-lookup"><span data-stu-id="d7257-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="d7257-170">Другие поставщики отключают объект, когда они не получают флаги для вызова **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="d7257-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="d7257-171">Некоторые свойства, обычно вычисляемые, не могут быть обработаны до тех пор, пока не будет вызван метод **SaveChanges** , а в некоторых случаях **он освободится**.</span><span class="sxs-lookup"><span data-stu-id="d7257-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="d7257-172">При выполнении массовых изменений, таких как сохранение вложений в нескольких сообщениях, отложить обработку ошибок путем установки флага МАПИ_ДЕФЕРРЕД_ЕРРОРС в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="d7257-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="d7257-173">Если вы сохраняете несколько вложений в несколько сообщений, сделайте один вызов **SaveChanges** на каждое вложение и один вызов **SaveChanges** для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7257-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="d7257-174">Установите флаг МАПИ_ДЕФЕРРЕД_ЕРРОРС для каждого вызова вложения и для всех сообщений, кроме последнего.</span><span class="sxs-lookup"><span data-stu-id="d7257-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="d7257-175">Если **SaveChanges** возвращает мапи_е_обжект_чанжед, проверьте, был ли изменен исходный объект.</span><span class="sxs-lookup"><span data-stu-id="d7257-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="d7257-176">Если да, предупредите пользователя, кто может запрашивать, что изменения перезапишут предыдущие изменения, или сохранить объект в другом месте.</span><span class="sxs-lookup"><span data-stu-id="d7257-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="d7257-177">Если исходный объект был удален, предупредите пользователя, чтобы предоставить ему возможность сохранить объект в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="d7257-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="d7257-178">Вы не можете вызвать **SaveChanges** с флагом форце_саве на открытом объекте, который был удален.</span><span class="sxs-lookup"><span data-stu-id="d7257-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="d7257-179">Если **SaveChanges** возвращает ошибку, объект, чьи изменения были сохранены, остается открытым, независимо от флагов, заданных в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d7257-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d7257-180">_UlFlags_ НОН_ЕМС_КСП_САВЕ и спамфилтер_онсаве могут не определяться в текущем загружаемом файле заголовков, в этом случае вы можете добавить его в код, используя следующие значения: _гт_`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="d7257-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="d7257-181">Дополнительную информацию можно узнать в статье [Сохранение свойств MAPI](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d7257-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7257-182">См. также</span><span class="sxs-lookup"><span data-stu-id="d7257-182">See also</span></span>



[<span data-ttu-id="d7257-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="d7257-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="d7257-184">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="d7257-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="d7257-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7257-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="d7257-186">Сохранение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="d7257-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

