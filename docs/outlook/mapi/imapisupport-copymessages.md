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
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591039"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="70f4f-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="70f4f-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="70f4f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70f4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70f4f-105">Копирование или перемещение сообщений из одной папки в другую папку.</span><span class="sxs-lookup"><span data-stu-id="70f4f-105">Copies or moves messages from one folder to another folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="70f4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70f4f-106">Parameters</span></span>

 <span data-ttu-id="70f4f-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="70f4f-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="70f4f-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к папке, содержащей сообщения, чтобы скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="70f4f-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="70f4f-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="70f4f-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="70f4f-110">[in] Указатель на папку, содержащую сообщения, чтобы скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="70f4f-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="70f4f-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="70f4f-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="70f4f-112">[in] Указатель на массив идентификаторов записи, чтобы указать сообщения, чтобы скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="70f4f-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="70f4f-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="70f4f-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="70f4f-114">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к папке назначения для копируемые или перемещения сообщений.</span><span class="sxs-lookup"><span data-stu-id="70f4f-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="70f4f-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="70f4f-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="70f4f-116">[in] Указатель на папку назначения для копируемые или перемещения сообщений.</span><span class="sxs-lookup"><span data-stu-id="70f4f-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="70f4f-117">Эта папка необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="70f4f-117">This folder must be open.</span></span>
    
 <span data-ttu-id="70f4f-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="70f4f-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="70f4f-119">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70f4f-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="70f4f-120">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70f4f-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="70f4f-121">Параметр _lpProgress_ используется только флаг MESSAGE_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="70f4f-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="70f4f-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="70f4f-122">_lpProgress_</span></span>
  
> <span data-ttu-id="70f4f-123">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70f4f-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="70f4f-124">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70f4f-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="70f4f-125">Параметр _lpProgress_ используется только флаг MESSAGE_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="70f4f-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="70f4f-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70f4f-126">_ulFlags_</span></span>
  
> <span data-ttu-id="70f4f-127">[in] Битовая маска флаги, который определяет, как выполнить операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="70f4f-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="70f4f-128">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="70f4f-128">The following flags can be set:</span></span>
    
<span data-ttu-id="70f4f-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="70f4f-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="70f4f-130">Запрос на отображение индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70f4f-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="70f4f-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="70f4f-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="70f4f-132">Сообщения должны быть перемещены, а не копируются.</span><span class="sxs-lookup"><span data-stu-id="70f4f-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="70f4f-133">Если MESSAGE_MOVE не задано, копируются сообщения.</span><span class="sxs-lookup"><span data-stu-id="70f4f-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="70f4f-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70f4f-134">Return value</span></span>

<span data-ttu-id="70f4f-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="70f4f-135">S_OK</span></span> 
  
> <span data-ttu-id="70f4f-136">Скопируйте или переместите операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="70f4f-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="70f4f-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="70f4f-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="70f4f-138">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="70f4f-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="70f4f-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="70f4f-139">Remarks</span></span>

<span data-ttu-id="70f4f-140">Метод **IMAPISupport::CopyMessages** реализуется для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="70f4f-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="70f4f-141">Поставщики хранилища сообщений можно вызвать **IMAPISupport::CopyMessages** в их реализации [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) для копирования или перемещения одно или несколько сообщений из одной папки в другую.</span><span class="sxs-lookup"><span data-stu-id="70f4f-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="70f4f-142">Как часть вызова **IMAPISupport::CopyMessages** поставщика хранилища сообщений можно указать, что MAPI должны отображать индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70f4f-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70f4f-143">См. также</span><span class="sxs-lookup"><span data-stu-id="70f4f-143">See also</span></span>



[<span data-ttu-id="70f4f-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="70f4f-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="70f4f-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="70f4f-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

