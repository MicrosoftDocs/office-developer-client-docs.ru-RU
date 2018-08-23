---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de5c98272c08c469acf23b0ecae7eac0a2d1bfe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592516"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="9066c-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="9066c-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="9066c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9066c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9066c-105">Удаляет вложения.</span><span class="sxs-lookup"><span data-stu-id="9066c-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9066c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9066c-106">Parameters</span></span>

 <span data-ttu-id="9066c-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="9066c-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="9066c-108">[in] Номер индекса для удаления вложения.</span><span class="sxs-lookup"><span data-stu-id="9066c-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="9066c-109">Это значение для свойства **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.</span><span class="sxs-lookup"><span data-stu-id="9066c-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="9066c-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9066c-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="9066c-111">[in] Дескриптор родительского окна все диалоговые окна и окна, этот метод отображает.</span><span class="sxs-lookup"><span data-stu-id="9066c-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="9066c-112">Параметр _ulUIParam_ игнорируется, пока флаг ATTACH_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9066c-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9066c-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9066c-113">_lpProgress_</span></span>
  
> <span data-ttu-id="9066c-114">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9066c-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9066c-115">Если в _lpProgress_передается значение NULL, поставщик хранения сообщений отображает индикатор выполнения с помощью объекта реализации интерфейса MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9066c-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="9066c-116">Параметр _lpProgress_ используется только флаг ATTACH_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="9066c-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9066c-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9066c-117">_ulFlags_</span></span>
  
> <span data-ttu-id="9066c-118">[in] Битовая маска флаги, определяющее отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9066c-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="9066c-119">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9066c-119">The following flag can be set:</span></span>
    
<span data-ttu-id="9066c-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9066c-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="9066c-121">Запрос на отображение индикатор выполнения как операция продолжается.</span><span class="sxs-lookup"><span data-stu-id="9066c-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9066c-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9066c-122">Return value</span></span>

<span data-ttu-id="9066c-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9066c-123">S_OK</span></span> 
  
> <span data-ttu-id="9066c-124">Вложение успешно удален.</span><span class="sxs-lookup"><span data-stu-id="9066c-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9066c-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="9066c-125">Remarks</span></span>

<span data-ttu-id="9066c-126">Метод **IMessage::DeleteAttach** удаляет вложения в сообщение.</span><span class="sxs-lookup"><span data-stu-id="9066c-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="9066c-127">До вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщение удаленного вложения не удаляется без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="9066c-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9066c-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9066c-128">Notes to callers</span></span>

<span data-ttu-id="9066c-129">До вызова метода **DeleteAttach**, вызовите метод **функции IUnknown::Release** для вложения и каждый из его потоков.</span><span class="sxs-lookup"><span data-stu-id="9066c-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="9066c-130">Поскольку удаление вложений может быть много времени, **DeleteAttach** обеспечивает механизм, индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9066c-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="9066c-131">Можно запросить отображение индикатор хода выполнения, передав указатель на [IMAPIProgress: IUnknown](imapiprogressiunknown.md) реализации или значение NULL, если у вас нет реализации.</span><span class="sxs-lookup"><span data-stu-id="9066c-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="9066c-132">Необходимо также указать дескриптор окна в параметр _ulUIParam_ и флаг ATTACH_DIALOG с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9066c-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9066c-133">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="9066c-133">MFCMAPI reference</span></span>

<span data-ttu-id="9066c-134">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="9066c-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9066c-135">**����**</span><span class="sxs-lookup"><span data-stu-id="9066c-135">**File**</span></span>|<span data-ttu-id="9066c-136">**�������**</span><span class="sxs-lookup"><span data-stu-id="9066c-136">**Function**</span></span>|<span data-ttu-id="9066c-137">**�����������**</span><span class="sxs-lookup"><span data-stu-id="9066c-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9066c-138">AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9066c-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="9066c-139">CAttachmentsDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="9066c-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="9066c-140">Mfcmapi (en) метод **IMessage::DeleteAttach** используется для удаления выбранного вложения.</span><span class="sxs-lookup"><span data-stu-id="9066c-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9066c-141">См. также</span><span class="sxs-lookup"><span data-stu-id="9066c-141">See also</span></span>



[<span data-ttu-id="9066c-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9066c-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="9066c-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9066c-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="9066c-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9066c-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

