---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412634"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="5176c-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="5176c-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="5176c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5176c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5176c-105">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="5176c-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="5176c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5176c-106">Parameters</span></span>

 <span data-ttu-id="5176c-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5176c-107">_lpInterface_</span></span>
  
> <span data-ttu-id="5176c-108">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к новому сообщению.</span><span class="sxs-lookup"><span data-stu-id="5176c-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="5176c-109">Допустимые идентификаторы интерфейса включают IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer и IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="5176c-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="5176c-110">Передача NULL заставляет поставщика хранения сообщений возвращать стандартный интерфейс [сообщения IMessage : IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="5176c-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="5176c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5176c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="5176c-112">[in] Битмаски флагов, которые контролируют, как создается сообщение.</span><span class="sxs-lookup"><span data-stu-id="5176c-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="5176c-113">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5176c-113">The following flags can be set:</span></span>
    
<span data-ttu-id="5176c-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="5176c-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="5176c-115">Указывает в личный магазин папок (PST) о том, что сообщение имеет право на обработку правил до того, как магазин извещение любого подслушавшего клиента о прибытии нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="5176c-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="5176c-116">Обработка правил применяется только к новым сообщениям, созданным на сервере, который не является Microsoft Exchange Server, так как Exchange Server обрабатывает правила для сообщений на сервере.</span><span class="sxs-lookup"><span data-stu-id="5176c-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="5176c-117">Поэтому поставщик или клиент, создавав сообщение, должен передать этот флаг в сочетании с сохранением сообщения с [помощью IMAPIPProp::SaveChanges](imapiprop-savechanges.md) с помощью NON_EMS_XP_SAVE, что указывает на то, что сервер не является Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5176c-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="5176c-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="5176c-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="5176c-119">Созданное сообщение должно быть включено в связанную таблицу содержимого, а не в стандартную таблицу содержимого.</span><span class="sxs-lookup"><span data-stu-id="5176c-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="5176c-120">Связанные сообщения скрыты от взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="5176c-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="5176c-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5176c-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5176c-122">**CreateMessage** можно добиться успеха, даже если операция создания не выполнена полностью.</span><span class="sxs-lookup"><span data-stu-id="5176c-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="5176c-123">Это означает, что новое сообщение может быть не сразу доступно вызываемой.</span><span class="sxs-lookup"><span data-stu-id="5176c-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="5176c-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="5176c-124">_lppMessage_</span></span>
  
> <span data-ttu-id="5176c-125">[вышел] Указатель на указатель на вновь созданное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5176c-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5176c-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5176c-126">Return value</span></span>

<span data-ttu-id="5176c-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="5176c-127">S_OK</span></span> 
  
> <span data-ttu-id="5176c-128">Сообщение было успешно создано.</span><span class="sxs-lookup"><span data-stu-id="5176c-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5176c-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="5176c-129">Remarks</span></span>

<span data-ttu-id="5176c-130">Метод **IMAPIFolder::CreateMessage** создает новое сообщение с общим или связанным содержимым и назначает идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="5176c-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="5176c-131">Идентификатор записи состоит из части, которая представляет поставщика магазина сообщений, и части, которая представляет отдельное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5176c-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5176c-132">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="5176c-132">Notes to implementers</span></span>

<span data-ttu-id="5176c-133">Вы можете выбрать, следует ли устанавливать все необходимые свойства сообщений в **CreateMessage** или в [методе IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="5176c-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="5176c-134">Не нужно делать эти свойства доступными до тех пор, пока не произошел успешный сохранения.</span><span class="sxs-lookup"><span data-stu-id="5176c-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="5176c-135">Дополнительные сведения о работе с связанной информацией см. в таблицах и таблицах содержимого, связанных с [папками.](contents-tables.md) [](folder-associated-information-tables.md)</span><span class="sxs-lookup"><span data-stu-id="5176c-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5176c-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5176c-136">Notes to callers</span></span>

<span data-ttu-id="5176c-137">Некоторые поставщики магазинов сообщений позволяют сразу после возвращения **CreateMessage** получить идентификатор записи нового сообщения; другие поставщики хранения сообщений задерживают его доступность до сберегания сообщения.</span><span class="sxs-lookup"><span data-stu-id="5176c-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="5176c-138">Так как не все поставщики хранения сообщений создают идентификатор входа для нового сообщения, пока вы не вызвали метод **IMAPIProp::SaveChanges,** вы можете не получить доступ к идентификатору записи при возвращении **CreateMessage.**</span><span class="sxs-lookup"><span data-stu-id="5176c-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="5176c-139">Кроме того, новое сообщение не может быть включено в таблицу содержимого папки до тех пор, пока не произойдет сохранение.</span><span class="sxs-lookup"><span data-stu-id="5176c-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="5176c-140">Ожидайте, что идентификатор записи, присвоенный новому сообщению, будет уникальным не только в текущем хранилище сообщений, но и, скорее всего, во всех открытых одновременно хранилищах сообщений.</span><span class="sxs-lookup"><span data-stu-id="5176c-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="5176c-141">Исключение из этого правила возникает, когда в профиле отображаются несколько записей для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="5176c-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="5176c-142">В результате хранилище сообщений открывается несколько раз, а идентификаторы записей дублируются.</span><span class="sxs-lookup"><span data-stu-id="5176c-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="5176c-143">Чтобы создать исходящие сообщения, вызовите метод **IMAPIFolder::CreateMessage** папки исходящие папки.</span><span class="sxs-lookup"><span data-stu-id="5176c-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="5176c-144">Если вы удалите папку, содержаную новое сообщение перед тем, как сообщение будет сохранено, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="5176c-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5176c-145">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5176c-145">MFCMAPI reference</span></span>

<span data-ttu-id="5176c-146">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5176c-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5176c-147">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5176c-147">**File**</span></span>|<span data-ttu-id="5176c-148">**Функция**</span><span class="sxs-lookup"><span data-stu-id="5176c-148">**Function**</span></span>|<span data-ttu-id="5176c-149">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="5176c-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5176c-150">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5176c-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="5176c-151">CFolder::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="5176c-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="5176c-152">MFCMAPI использует **метод IMAPIFolder::CreateMessage** для создания и сохранения нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="5176c-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5176c-153">См. также</span><span class="sxs-lookup"><span data-stu-id="5176c-153">See also</span></span>



[<span data-ttu-id="5176c-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5176c-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="5176c-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5176c-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="5176c-156">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5176c-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

