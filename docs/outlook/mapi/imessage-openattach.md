---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 48df5362106e849f061b0797736fad82fafa6584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588715"
---
# <a name="imessageopenattach"></a><span data-ttu-id="7ef84-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="7ef84-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="7ef84-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ef84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ef84-105">Открывает вложение.</span><span class="sxs-lookup"><span data-stu-id="7ef84-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="7ef84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ef84-106">Parameters</span></span>

 <span data-ttu-id="7ef84-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="7ef84-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="7ef84-108">[in] Номер индекса вложения, чтобы открыть, сохраненный в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.</span><span class="sxs-lookup"><span data-stu-id="7ef84-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="7ef84-109">Этот номер индекса вложения в сообщении уникально идентифицирует допустимо только в контексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="7ef84-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="7ef84-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7ef84-110">_lpInterface_</span></span>
  
> <span data-ttu-id="7ef84-111">[in] Указатель на идентификатор интерфейса (ИД интерфейса), представляющий интерфейс, который будет использоваться для доступа к вложение.</span><span class="sxs-lookup"><span data-stu-id="7ef84-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="7ef84-112">Передача значение NULL, приводит к стандартным интерфейсом вложения или **IAttach**, возвращаемых.</span><span class="sxs-lookup"><span data-stu-id="7ef84-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="7ef84-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ef84-113">_ulFlags_</span></span>
  
> <span data-ttu-id="7ef84-114">[in] Битовая маска флаги, который определяет, как открыть вложение.</span><span class="sxs-lookup"><span data-stu-id="7ef84-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="7ef84-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="7ef84-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="7ef84-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7ef84-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="7ef84-117">Запрашивает открывать вложения с разрешениями максимальное сети, разрешенных для пользователя и приложения максимальное клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="7ef84-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="7ef84-118">Например если клиент имеет разрешение на чтение и запись, вложение должен быть открыт с разрешением на чтение и запись; Если клиент имеет доступ только для чтения, следует открыть вложение с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7ef84-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="7ef84-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7ef84-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7ef84-120">Позволяет **OpenAttach** для возврата успешно, возможно перед вложение доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="7ef84-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="7ef84-121">Если вложение не поддерживается, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="7ef84-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="7ef84-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7ef84-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7ef84-123">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7ef84-123">Requests read/write permission.</span></span> <span data-ttu-id="7ef84-124">По умолчанию открытия вложений с доступом только для чтения и клиенты не должны работать предполагается, что что назначено разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7ef84-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="7ef84-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="7ef84-125">_lppAttach_</span></span>
  
> <span data-ttu-id="7ef84-126">[out] Указатель на указатель открыть вложение.</span><span class="sxs-lookup"><span data-stu-id="7ef84-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ef84-127">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7ef84-127">Return value</span></span>

<span data-ttu-id="7ef84-128">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7ef84-128">S_OK</span></span> 
  
> <span data-ttu-id="7ef84-129">Вложение был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="7ef84-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ef84-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ef84-130">Remarks</span></span>

<span data-ttu-id="7ef84-131">Метод **IMessage::OpenAttach** открывает вложения сообщения.</span><span class="sxs-lookup"><span data-stu-id="7ef84-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7ef84-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7ef84-132">Notes to callers</span></span>

<span data-ttu-id="7ef84-133">Чтобы открыть вложения, имеется доступ к номеру вложения или свойство **PR_ATTACH_NUM** .</span><span class="sxs-lookup"><span data-stu-id="7ef84-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="7ef84-134">Вызов [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) для получения таблицы вложений сообщений и найдите строку, которая представляет вложение, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="7ef84-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="7ef84-135">Для получения дополнительных сведений в разделе [Открытие вложения](opening-an-attachment.md) .</span><span class="sxs-lookup"><span data-stu-id="7ef84-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="7ef84-136">Не пытайтесь открыть одного вложения несколько раз. результаты, значение undefined и зависящие от поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ef84-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="7ef84-137">Можно запросить открывать вложения в режиме чтения и записи, а не в режиме только для чтения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ef84-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="7ef84-138">Тем не менее ли вложение фактически открывается в режиме чтения и записи зависит от поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ef84-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="7ef84-139">Можно либо попытка изменить вложение, Подготовка для обработки возможных сбоев или установите флажок для уровня доступа, которые были предоставлены извлекая свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) вложений, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="7ef84-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ef84-140">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="7ef84-140">MFCMAPI reference</span></span>

<span data-ttu-id="7ef84-141">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="7ef84-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ef84-142">**����**</span><span class="sxs-lookup"><span data-stu-id="7ef84-142">**File**</span></span>|<span data-ttu-id="7ef84-143">**�������**</span><span class="sxs-lookup"><span data-stu-id="7ef84-143">**Function**</span></span>|<span data-ttu-id="7ef84-144">**�����������**</span><span class="sxs-lookup"><span data-stu-id="7ef84-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ef84-145">Используется для AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7ef84-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="7ef84-146">CAttachmentsDlg::OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="7ef84-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="7ef84-147">Mfcmapi (en) использует метод **IMessage::OpenAttach** для открытия вложения объектов</span><span class="sxs-lookup"><span data-stu-id="7ef84-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ef84-148">См. также</span><span class="sxs-lookup"><span data-stu-id="7ef84-148">See also</span></span>



[<span data-ttu-id="7ef84-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7ef84-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="7ef84-150">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7ef84-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

