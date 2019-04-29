---
title: Имессажеопенаттач
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
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405900"
---
# <a name="imessageopenattach"></a><span data-ttu-id="f248e-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="f248e-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="f248e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f248e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f248e-105">Открывает вложение.</span><span class="sxs-lookup"><span data-stu-id="f248e-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="f248e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f248e-106">Parameters</span></span>

 <span data-ttu-id="f248e-107">_Улаттачментнум_</span><span class="sxs-lookup"><span data-stu-id="f248e-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="f248e-108">возврата Номер индекса открываемого вложения, хранящегося в свойстве вложения **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f248e-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="f248e-109">Этот номер индекса однозначно определяет вложение в сообщении и является допустимым только в контексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="f248e-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="f248e-110">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="f248e-110">_lpInterface_</span></span>
  
> <span data-ttu-id="f248e-111">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к вложению.</span><span class="sxs-lookup"><span data-stu-id="f248e-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="f248e-112">Передача результатов NULL в стандартный интерфейс вложения (или **иаттач**) возвращается.</span><span class="sxs-lookup"><span data-stu-id="f248e-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="f248e-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f248e-113">_ulFlags_</span></span>
  
> <span data-ttu-id="f248e-114">возврата Битовая маска флагов, определяющих способ открытия вложения.</span><span class="sxs-lookup"><span data-stu-id="f248e-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="f248e-115">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f248e-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="f248e-116">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="f248e-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="f248e-117">ЗаПрашивает открытие вложения с максимальными сетевыми разрешениями, разрешенными для пользователя, и максимальным доступом к клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="f248e-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="f248e-118">Например, если у клиента есть разрешение на чтение и запись, вложение должно быть открыто с разрешением на чтение и запись; Если клиент имеет доступ только для чтения, вложение должно быть открыто с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f248e-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="f248e-119">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="f248e-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f248e-120">Разрешает успешное возвращение **опенаттач** , возможно, перед тем, как вложение будет полностью доступно для вызывающего клиента.</span><span class="sxs-lookup"><span data-stu-id="f248e-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="f248e-121">Если вложение недоступно, выполнение последующего вызова этого метода может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="f248e-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="f248e-122">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="f248e-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f248e-123">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="f248e-123">Requests read/write permission.</span></span> <span data-ttu-id="f248e-124">По умолчанию вложения открываются с доступом только для чтения, и клиенты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="f248e-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="f248e-125">_Лппаттач_</span><span class="sxs-lookup"><span data-stu-id="f248e-125">_lppAttach_</span></span>
  
> <span data-ttu-id="f248e-126">вышли Указатель на указатель на открытое вложение.</span><span class="sxs-lookup"><span data-stu-id="f248e-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f248e-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f248e-127">Return value</span></span>

<span data-ttu-id="f248e-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="f248e-128">S_OK</span></span> 
  
> <span data-ttu-id="f248e-129">Вложение успешно открыто.</span><span class="sxs-lookup"><span data-stu-id="f248e-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f248e-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="f248e-130">Remarks</span></span>

<span data-ttu-id="f248e-131">Метод **iMessage:: опенаттач** открывает вложение сообщения.</span><span class="sxs-lookup"><span data-stu-id="f248e-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f248e-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f248e-132">Notes to callers</span></span>

<span data-ttu-id="f248e-133">Чтобы открыть вложение, необходимо иметь доступ к его номеру вложения или свойству **пр_аттач_нум** .</span><span class="sxs-lookup"><span data-stu-id="f248e-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="f248e-134">Call [iMessage:: жетаттачменттабле](imessage-getattachmenttable.md) , чтобы получить таблицу вложений сообщения и найти строку, представляющую открываемое вложение.</span><span class="sxs-lookup"><span data-stu-id="f248e-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="f248e-135">Дополнительную информацию [можно узнать в разделе Открытие вложения](opening-an-attachment.md) .</span><span class="sxs-lookup"><span data-stu-id="f248e-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="f248e-136">Не пытайтесь открыть одно вложение несколько раз; результаты не определены и зависят от поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f248e-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="f248e-137">Вы можете запросить открытие вложения в режиме чтения и записи, а не в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f248e-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="f248e-138">Тем не менее, может ли вложение быть открыто в режиме чтения и записи, до поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f248e-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="f248e-139">Вы можете либо попытаться изменить вложение, подготовиться к обработке возможного сбоя, либо проверить уровень доступа, предоставленный при получении свойства вложения ( \*\*\*\* [PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)), если он доступен.</span><span class="sxs-lookup"><span data-stu-id="f248e-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f248e-140">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f248e-140">MFCMAPI reference</span></span>

<span data-ttu-id="f248e-141">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f248e-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f248e-142">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f248e-142">**File**</span></span>|<span data-ttu-id="f248e-143">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f248e-143">**Function**</span></span>|<span data-ttu-id="f248e-144">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f248e-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f248e-145">Аттачментсдлг. cpp используется для</span><span class="sxs-lookup"><span data-stu-id="f248e-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="f248e-146">Каттачментсдлг:: Опенитемпроп</span><span class="sxs-lookup"><span data-stu-id="f248e-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="f248e-147">MFCMAPI использует метод **iMessage:: опенаттач** , чтобы открыть объекты вложений,</span><span class="sxs-lookup"><span data-stu-id="f248e-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f248e-148">См. также</span><span class="sxs-lookup"><span data-stu-id="f248e-148">See also</span></span>



[<span data-ttu-id="f248e-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f248e-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="f248e-150">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f248e-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

