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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398845"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="8f9ad-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8f9ad-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="8f9ad-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f9ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f9ad-105">Выполняет постоянное все изменения, внесенные в объект с момента последней операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8f9ad-106">���������</span><span class="sxs-lookup"><span data-stu-id="8f9ad-106">Parameters</span></span>

 <span data-ttu-id="8f9ad-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8f9ad-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8f9ad-108">[in] Битовая маска флаги, который определяет, что происходит при вызове метода **IMAPIProp::SaveChanges** объекта.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="8f9ad-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="8f9ad-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="8f9ad-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="8f9ad-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="8f9ad-111">Указывает, что сообщение не было доставлено из Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="8f9ad-112">Этот флаг следует использовать в сочетании с методом [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) и ITEMPROC_FORCE флаг, указывающий хранилище PST-файлов, который сообщение подходит для правила обработки перед любой уведомляет хранилище файлов (PST) личных папок прослушивающий клиент поступления сообщения.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="8f9ad-113">Правила на сообщение будет уже обработаны этот правила обработки применяется только к новые сообщения, созданные с помощью [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) на сервере, который не является сервером Exchange Server, в этом случае на сервере Exchange.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="8f9ad-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="8f9ad-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="8f9ad-115">Изменения будут записаны в объект, переопределение любые предыдущие изменения, внесенные в объект, и объект должен быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="8f9ad-116">Разрешение на чтение/запись необходимо установить для успешного выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="8f9ad-117">Флаг FORCE_SAVE используется после предыдущего вызова **SaveChanges** возвращается MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="8f9ad-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="8f9ad-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="8f9ad-119">Изменения должны быть зафиксированы и объекта должно быть открытым для чтения.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="8f9ad-120">Не дополнительные будут изменены.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="8f9ad-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="8f9ad-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="8f9ad-122">Изменения должны быть зафиксированы и объекта должно быть открытым для разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="8f9ad-123">Этот флаг обычно задается после первого открытия объекта для разрешения на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="8f9ad-124">Последующие изменения объекта разрешены.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="8f9ad-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8f9ad-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8f9ad-126">Разрешает **SaveChanges** для возврата успешно, возможно до полностью применить изменения.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="8f9ad-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="8f9ad-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="8f9ad-128">Включение защиты от нежелательной почты фильтрации на сообщение, которое сохраняется.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="8f9ad-129">Поддержка фильтрации нежелательной почты доступна только в том случае, если тип адреса электронной почты отправителя Simple Mail Transfer Protocol (SMTP), и сообщение сохраняется в хранилище для файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="8f9ad-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f9ad-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f9ad-130">Return value</span></span>

<span data-ttu-id="8f9ad-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f9ad-131">S_OK</span></span> 
  
> <span data-ttu-id="8f9ad-132">Стремление изменения успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="8f9ad-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8f9ad-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8f9ad-134">**SaveChanges** невозможно сохранить объект open для разрешения доступа только для чтения если KEEP_OPEN_READONLY set или разрешение на чтение/запись, если значение KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="8f9ad-135">Изменения не фиксируются.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-135">No changes are committed.</span></span> 
    
<span data-ttu-id="8f9ad-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="8f9ad-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="8f9ad-137">Объект изменился с момента его открытия.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="8f9ad-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="8f9ad-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="8f9ad-139">Объект был удален, поскольку он был открыт.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8f9ad-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f9ad-140">Remarks</span></span>

<span data-ttu-id="8f9ad-141">Метод **IMAPIProp::SaveChanges** вносятся изменения свойства было постоянным для объектов, которые поддерживают модели транзакций обработки, такие как сообщения, вложения, контейнеров адресной книги, и системы обмена сообщениями объектов-пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="8f9ad-142">Объекты, которые не поддерживают транзакции, как папки, хранилищ сообщений и разделах профилей, внесите изменения постоянное немедленно.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="8f9ad-143">Вызов **SaveChanges** не требуется.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="8f9ad-144">Так как поставщиков услуг не нужно создать запись идентификатора для объектов, пока не были сохранены все свойства, свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) могут быть недоступны до после его метод **SaveChanges** был вызван.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="8f9ad-145">Некоторые поставщики Подождите, пока флаг KEEP_OPEN_READONLY установлен на вызов **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="8f9ad-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="8f9ad-146">KEEP_OPEN_READONLY означает, что изменения будут сохраняться в текущий звонок будет последних изменений, внесенных в объекте.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="8f9ad-147">Некоторые реализации хранилища сообщений выполнение не показывать вновь созданный сообщений в папке до клиента сохранения сообщение изменяется с помощью **SaveChanges** и освобождает объекты сообщений с помощью метода [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8f9ad-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="8f9ad-148">Кроме того некоторые реализации объекта не удается создать свойство **PR_ENTRYID** для только что созданный объект до того времени, после того как был вызван метод **SaveChanges** , и некоторые делать это только после **SaveChanges** вызова с помощью KEEP_OPEN_READONLY Задайте в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8f9ad-149">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="8f9ad-149">Notes to implementers</span></span>

<span data-ttu-id="8f9ad-150">Если вы получите флаг KEEP_OPEN_READONLY, вы можете отправляемых из объекта доступ для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="8f9ad-151">Тем не менее поставщик может не оставляйте объекта в состояние только для чтения при передаче флага KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="8f9ad-152">Когда клиент сохраняет несколько вложений для нескольких сообщений, он вызывает метод **SaveChanges** для каждого вложения и каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="8f9ad-153">Клиенты часто устанавливающей MAPI_DEFERRED_ERRORS для каждого из них, за исключением последним.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="8f9ad-154">Ошибки с последнего вызова или более ранних звонки можно вернуть.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="8f9ad-155">Можно даже игнорировать флаг.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="8f9ad-156">Если вместе с MAPI_DEFERRED_ERRORS KEEP_OPEN_READWRITE или KEEP_OPEN_READONLY, можно пропустить ошибка отсрочке запроса.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="8f9ad-157">Если MAPI_DEFERRED_ERRORS не установлен в _ulFlags_, один из ранее отложенная ошибки могут быть возвращены для этого вызова **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="8f9ad-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="8f9ad-158">Обеспечивает ли поставщик удаленного транспорта функциональным реализация этого метода является необязательной и зависит от других варианты проектирования в реализации.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="8f9ad-159">Если этот метод реализации, сделайте согласно документации по.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="8f9ad-160">Так как папки и объекты состояния не выполняются, по крайней мере реализации поставщика транспорта удаленного **SaveChanges** должен возвращать значение S_OK без фактического выполнения действий.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8f9ad-161">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8f9ad-161">Notes to callers</span></span>

<span data-ttu-id="8f9ad-162">Если клиент проходит KEEP_OPEN_READONLY, вызывает метод [IMAPIProp::SetProps](imapiprop-setprops.md) и затем вызывает метод **SaveChanges** , ту же реализацию может завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="8f9ad-163">После получения MAPI_E_NO_ACCESS от звонка в которых KEEP_OPEN_READWRITE, будут иметь разрешение на чтение и запись к объекту.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="8f9ad-164">Можно вызвать **SaveChanges** еще раз, передав флаг KEEP_OPEN_READONLY или флаги не со KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="8f9ad-165">Поддерживает ли поставщик флаг KEEP_OPEN_READWRITE зависит от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="8f9ad-166">Чтобы указать только вызова следует обратить внимание на объекте после **SaveChanges** **функции IUnknown::Release**, задайте флаги для параметра _ulFlags_ не.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8f9ad-167">Ошибка из **SaveChanges** указывает на то, что его нельзя было ожидающие изменения постоянной.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="8f9ad-168">Различных поставщиков обработки отсутствия флаги на вызов **SaveChanges** по-разному.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="8f9ad-169">Некоторые поставщики обрабатывать это состояние так же, как KEEP_OPEN_READONLY; Прочие интерпретировать то же, что KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="8f9ad-170">По-прежнему других поставщиков завершение работы объекта, когда они не получают флаги на вызов **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="8f9ad-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="8f9ad-171">Некоторые свойства, обычно вычисленные свойства не может обрабатываться до вызова метода **SaveChanges** и, в некоторых случаях **выпуска**.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="8f9ad-172">При внесении массового изменения, такие как сохранение вложений на несколько сообщений отложите Ошибка обработки, установив флаг MAPI_DEFERRED_ERRORS в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="8f9ad-173">При сохранении нескольких вложения на несколько сообщений, внесите один **SaveChanges** звонков для каждого вложения и один **SaveChanges** звонков для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="8f9ad-174">Установите флаг MAPI_DEFERRED_ERRORS для каждого вызова вложения, а также для всех сообщений за исключением последним.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="8f9ad-175">Если **SaveChanges** возвращает MAPI_E_OBJECT_CHANGED, проверьте, были ли изменены исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="8f9ad-176">Если это так, Предупреждайте пользователя, который можно либо запросить, что изменения перезаписи предыдущей изменения или сохранить объект в другом месте.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="8f9ad-177">Если исходный объект был удален, Предупреждайте пользователя, который будет их возможности, чтобы сохранить объект в другом месте.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="8f9ad-178">Не может вызывать **SaveChanges** с флагом FORCE_SAVE open объекта, который был удален.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="8f9ad-179">Если **SaveChanges** возвращает ошибку, откройте объект, чьи изменения были сохранения остается с текущими настройками вне зависимости от набора с помощью параметра _ulFlags_ флагов.</span><span class="sxs-lookup"><span data-stu-id="8f9ad-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8f9ad-180">_UlFlags_ NON_EMS_XP_SAVE и SPAMFILTER_ONSAVE не может быть определен в файле загружаемых заголовка в настоящий момент, в этом случае можно добавить его в код, используя следующие значения: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="8f9ad-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="8f9ad-181">Для получения дополнительных сведений см [Сохранения свойств MAPI](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8f9ad-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8f9ad-182">См. также</span><span class="sxs-lookup"><span data-stu-id="8f9ad-182">See also</span></span>



[<span data-ttu-id="8f9ad-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="8f9ad-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="8f9ad-184">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="8f9ad-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="8f9ad-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f9ad-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="8f9ad-186">Сохранение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="8f9ad-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

