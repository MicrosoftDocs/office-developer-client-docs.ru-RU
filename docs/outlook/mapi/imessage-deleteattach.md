---
title: Имессажеделетеаттач
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
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430709"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="604de-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="604de-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="604de-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="604de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="604de-105">Удаляет вложение.</span><span class="sxs-lookup"><span data-stu-id="604de-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="604de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="604de-106">Parameters</span></span>

 <span data-ttu-id="604de-107">_Улаттачментнум_</span><span class="sxs-lookup"><span data-stu-id="604de-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="604de-108">возврата Номер индекса удаляемого вложения.</span><span class="sxs-lookup"><span data-stu-id="604de-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="604de-109">Это значение для свойства **пр_аттач_нум** вложения ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="604de-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="604de-110">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="604de-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="604de-111">возврата Дескриптор родительского окна всех диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="604de-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="604de-112">Параметр _улуипарам_ игнорируется, если не установлен флаг аттач_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="604de-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="604de-113">_Лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="604de-113">_lpProgress_</span></span>
  
> <span data-ttu-id="604de-114">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="604de-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="604de-115">Если в _лппрогресс_переДАЕТСЯ значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="604de-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="604de-116">Параметр _лппрогресс_ игнорируется, если не установлен флаг Аттач_диалог в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="604de-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="604de-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="604de-117">_ulFlags_</span></span>
  
> <span data-ttu-id="604de-118">возврата Битовая маска флагов, которые управляют отображением пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="604de-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="604de-119">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="604de-119">The following flag can be set:</span></span>
    
<span data-ttu-id="604de-120">АТТАЧ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="604de-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="604de-121">ЗаПрашивает отображение индикатора хода выполнения при выполнении операции.</span><span class="sxs-lookup"><span data-stu-id="604de-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="604de-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="604de-122">Return value</span></span>

<span data-ttu-id="604de-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="604de-123">S_OK</span></span> 
  
> <span data-ttu-id="604de-124">Вложение успешно удалено.</span><span class="sxs-lookup"><span data-stu-id="604de-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="604de-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="604de-125">Remarks</span></span>

<span data-ttu-id="604de-126">Метод **iMessage::D елетеаттач** удаляет вложение из сообщения.</span><span class="sxs-lookup"><span data-stu-id="604de-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="604de-127">Удаленное вложение не удаляется окончательно до тех пор, пока не будет вызван метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="604de-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="604de-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="604de-128">Notes to callers</span></span>

<span data-ttu-id="604de-129">Перед вызовом **делетеаттач**вызовите метод **IUnknown:: Release** для вложения и всех его потоков.</span><span class="sxs-lookup"><span data-stu-id="604de-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="604de-130">Так как удаление вложения может быть длительным процессом, **делетеаттач** предоставляет механизм, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="604de-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="604de-131">Вы можете запросить отображение индикатора хода выполнения путем передачи указателя на [IMAPIProgress: реализация IUnknown](imapiprogressiunknown.md) или значение null, если у вас нет реализации.</span><span class="sxs-lookup"><span data-stu-id="604de-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="604de-132">Кроме того, необходимо указать дескриптор окна в параметре _улуипарам_ и флаг аттач_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="604de-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="604de-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="604de-133">MFCMAPI reference</span></span>

<span data-ttu-id="604de-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="604de-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="604de-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="604de-135">**File**</span></span>|<span data-ttu-id="604de-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="604de-136">**Function**</span></span>|<span data-ttu-id="604de-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="604de-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="604de-138">Аттачментсдлг. cpp</span><span class="sxs-lookup"><span data-stu-id="604de-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="604de-139">Каттачментсдлг:: Онделетеселектедитем</span><span class="sxs-lookup"><span data-stu-id="604de-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="604de-140">MFCMAPI использует метод **iMessage::D елетеаттач** , чтобы удалить выбранное вложение.</span><span class="sxs-lookup"><span data-stu-id="604de-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="604de-141">См. также</span><span class="sxs-lookup"><span data-stu-id="604de-141">See also</span></span>



[<span data-ttu-id="604de-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="604de-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="604de-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="604de-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="604de-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="604de-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

