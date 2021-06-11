---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405158"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="be64f-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="be64f-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="be64f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be64f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be64f-105">Копирует или перемещает сообщения из одной папки в другую.</span><span class="sxs-lookup"><span data-stu-id="be64f-105">Copies or moves messages from one folder to another folder.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="be64f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="be64f-106">Parameters</span></span>

 <span data-ttu-id="be64f-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="be64f-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="be64f-108">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к папке, которая содержит сообщения, которые будут скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="be64f-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="be64f-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="be64f-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="be64f-110">[in] Указатель на папку, содержаную скопированные или перемещенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="be64f-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="be64f-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="be64f-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="be64f-112">[in] Указатель на массив идентификаторов записей, которые определяют сообщения, которые будут скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="be64f-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="be64f-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="be64f-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="be64f-114">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к папке назначения для скопированные или перенесенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="be64f-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="be64f-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="be64f-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="be64f-116">[in] Указатель на папку назначения для скопированные или перенесенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="be64f-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="be64f-117">Эта папка должна быть открыта.</span><span class="sxs-lookup"><span data-stu-id="be64f-117">This folder must be open.</span></span>
    
 <span data-ttu-id="be64f-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="be64f-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="be64f-119">[in] Указатель на объект progress, отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="be64f-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="be64f-120">Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI.</span><span class="sxs-lookup"><span data-stu-id="be64f-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="be64f-121">Параметр  _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="be64f-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="be64f-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="be64f-122">_lpProgress_</span></span>
  
> <span data-ttu-id="be64f-123">[in] Указатель на объект progress, отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="be64f-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="be64f-124">Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI.</span><span class="sxs-lookup"><span data-stu-id="be64f-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="be64f-125">Параметр  _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="be64f-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="be64f-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be64f-126">_ulFlags_</span></span>
  
> <span data-ttu-id="be64f-127">[in] Немного флагов, которые контролируют выполнение операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="be64f-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="be64f-128">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="be64f-128">The following flags can be set:</span></span>
    
<span data-ttu-id="be64f-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="be64f-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="be64f-130">Запрашивает отображение индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="be64f-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="be64f-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="be64f-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="be64f-132">Сообщения должны быть перемещены, а не скопированы.</span><span class="sxs-lookup"><span data-stu-id="be64f-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="be64f-133">Если MESSAGE_MOVE не установлено, сообщения копируется.</span><span class="sxs-lookup"><span data-stu-id="be64f-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be64f-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be64f-134">Return value</span></span>

<span data-ttu-id="be64f-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="be64f-135">S_OK</span></span> 
  
> <span data-ttu-id="be64f-136">Операция копирования или перемещения была успешной.</span><span class="sxs-lookup"><span data-stu-id="be64f-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="be64f-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="be64f-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="be64f-138">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="be64f-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="be64f-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="be64f-139">Remarks</span></span>

<span data-ttu-id="be64f-140">Метод **IMAPISupport::CopyMessages** реализован для объектов поддержки поставщиков сообщений.</span><span class="sxs-lookup"><span data-stu-id="be64f-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="be64f-141">Поставщики магазинов сообщений могут вызывать **IMAPISupport::CopyMessages** при реализации [IMAPIFolder::CopyMessages,](imapifolder-copymessages.md) чтобы скопировать или переместить одно или несколько сообщений из одной папки в другую.</span><span class="sxs-lookup"><span data-stu-id="be64f-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="be64f-142">В рамках вызова **IMAPISupport::CopyMessages** поставщик магазина сообщений может указать, что MAPI должен отображать индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="be64f-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be64f-143">См. также</span><span class="sxs-lookup"><span data-stu-id="be64f-143">See also</span></span>



[<span data-ttu-id="be64f-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="be64f-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="be64f-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="be64f-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

