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
ms.openlocfilehash: 8d7e6dfbf9e6a751845adb2319b66462bcde651f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808849"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="1ddd5-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="1ddd5-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="1ddd5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ddd5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ddd5-105">Создает новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="1ddd5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ddd5-106">Parameters</span></span>

 <span data-ttu-id="1ddd5-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1ddd5-107">_lpInterface_</span></span>
  
> <span data-ttu-id="1ddd5-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="1ddd5-109">Идентификаторы допустимого интерфейса включают IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer и IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="1ddd5-110">Значение NULL вызывает поставщика хранилища сообщений для возврата интерфейс стандартные сообщения [IMessage: IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="1ddd5-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="1ddd5-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ddd5-111">_ulFlags_</span></span>
  
> <span data-ttu-id="1ddd5-112">[in] Битовая маска флаги, который определяет, каким образом создается сообщение.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="1ddd5-113">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="1ddd5-113">The following flags can be set:</span></span>
    
<span data-ttu-id="1ddd5-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="1ddd5-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="1ddd5-115">Указывает, чтобы в хранилище личных папок (PST), что сообщение подходит для правила обработки перед хранилище уведомляет любого прослушивания клиента о получении нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="1ddd5-116">Правила обработки только применяется для новых сообщений, созданных на сервере, который не является Microsoft Exchange Server, так как Exchange Server обрабатывает правила для сообщений на сервере.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="1ddd5-117">Таким образом поставщика или клиента при создании сообщения должен пройти этот флаг в сочетании с сохранением сообщение с [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) с помощью NON_EMS_XP_SAVE, это означает, что сервер не является сервером Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="1ddd5-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="1ddd5-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="1ddd5-119">Сообщение будет создан должно быть включено в связанное содержимое таблицы, а не в таблице стандартных содержимое.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="1ddd5-120">Связанные сообщения скрыты от взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="1ddd5-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1ddd5-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1ddd5-122">**CreateMessage** может даже в том случае, если операция создания выполнена не полностью.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="1ddd5-123">Это означает, что новое сообщение не может быть сразу становятся доступными для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="1ddd5-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="1ddd5-124">_lppMessage_</span></span>
  
> <span data-ttu-id="1ddd5-125">[out] Указатель на указатель на только что созданный сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ddd5-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1ddd5-126">Return value</span></span>

<span data-ttu-id="1ddd5-127">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1ddd5-127">S_OK</span></span> 
  
> <span data-ttu-id="1ddd5-128">Сообщение было успешно создано.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ddd5-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="1ddd5-129">Remarks</span></span>

<span data-ttu-id="1ddd5-130">Метод **IMAPIFolder::CreateMessage** создает новое сообщение с универсальный или связанный контент и назначает идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="1ddd5-131">Идентификатор записи состоит из части, который представляет поставщика хранилища сообщений и, представляющий отдельных сообщений.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1ddd5-132">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1ddd5-132">Notes to implementers</span></span>

<span data-ttu-id="1ddd5-133">Можно ли задать все свойства необходимые сообщения в **CreateMessage** или в метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщений.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="1ddd5-134">Необходимо внести эти свойства доступны только после успешного сохранения произошла.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="1ddd5-135">Дополнительные сведения о работе с связанные сведения см [сведения о Folder-Associated](folder-associated-information-tables.md) и [Содержимое таблицы](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1ddd5-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1ddd5-136">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1ddd5-136">Notes to callers</span></span>

<span data-ttu-id="1ddd5-137">Некоторые поставщики хранилища сообщений разрешить запись идентификатор нового сообщения будут доступны сразу же после возвращает **CreateMessage** ; прочие службы хранилища сообщений отложить его доступность до сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="1ddd5-138">Так как не все поставщики хранилища сообщений создающего запись идентификатор нового сообщения до вызова метода **IMAPIProp::SaveChanges** сообщение, не удается получить доступ к идентификатор записи при возврате **CreateMessage** .</span><span class="sxs-lookup"><span data-stu-id="1ddd5-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="1ddd5-139">Кроме того новое сообщение могут отсутствовать в таблице содержимое папки до сохранения.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="1ddd5-140">Ожидается, что запись идентификатор, назначенный новое сообщение быть уникальными не только в хранилище текущего сообщения, но скорее всего, во всех хранилищ сообщений, которые открыты в то же время.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="1ddd5-141">Одно исключение из этого правила происходит, когда несколько записей для хранения сообщений отображаются в профиле.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="1ddd5-142">После этого хранилища сообщений для открытия несколько раз и идентификаторы записей дублирование.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="1ddd5-143">Чтобы создать исходящих сообщений, вызовите метод **IMAPIFolder::CreateMessage** папке Исходящие.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="1ddd5-144">Если удалить папку, содержащую нового сообщения перед сохранением сообщения, результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ddd5-145">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="1ddd5-145">MFCMAPI reference</span></span>

<span data-ttu-id="1ddd5-146">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ddd5-147">**����**</span><span class="sxs-lookup"><span data-stu-id="1ddd5-147">**File**</span></span>|<span data-ttu-id="1ddd5-148">**�������**</span><span class="sxs-lookup"><span data-stu-id="1ddd5-148">**Function**</span></span>|<span data-ttu-id="1ddd5-149">**�����������**</span><span class="sxs-lookup"><span data-stu-id="1ddd5-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ddd5-150">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1ddd5-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="1ddd5-151">CFolder::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="1ddd5-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="1ddd5-152">Mfcmapi (en) использует метод **IMAPIFolder::CreateMessage** для создания и сохранения нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ddd5-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ddd5-153">См. также</span><span class="sxs-lookup"><span data-stu-id="1ddd5-153">See also</span></span>



[<span data-ttu-id="1ddd5-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="1ddd5-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="1ddd5-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1ddd5-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="1ddd5-156">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1ddd5-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

