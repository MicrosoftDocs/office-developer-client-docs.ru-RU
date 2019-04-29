---
title: Имаписуппорткопимессажес
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
# <a name="imapisupportcopymessages"></a><span data-ttu-id="ca700-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ca700-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="ca700-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca700-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca700-105">Копирует или перемещает сообщения из одной папки в другую.</span><span class="sxs-lookup"><span data-stu-id="ca700-105">Copies or moves messages from one folder to another folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ca700-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca700-106">Parameters</span></span>

 <span data-ttu-id="ca700-107">_ЛпсрЦинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="ca700-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="ca700-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к папке, содержащей сообщения, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="ca700-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="ca700-109">_Лпсркфолдер_</span><span class="sxs-lookup"><span data-stu-id="ca700-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="ca700-110">возврата Указатель на папку, содержащую копируемые или перемещаемые сообщения.</span><span class="sxs-lookup"><span data-stu-id="ca700-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="ca700-111">_Лпмсглист_</span><span class="sxs-lookup"><span data-stu-id="ca700-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="ca700-112">возврата Указатель на массив идентификаторов записей, определяющих копируемые или перемещаемые сообщения.</span><span class="sxs-lookup"><span data-stu-id="ca700-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="ca700-113">_Лпдестинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="ca700-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="ca700-114">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к папке назначения для скопированных или перемещенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="ca700-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="ca700-115">_Лпдестфолдер_</span><span class="sxs-lookup"><span data-stu-id="ca700-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="ca700-116">возврата Указатель на папку назначения для скопированных или перемещенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="ca700-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="ca700-117">Эта папка должна быть открыта.</span><span class="sxs-lookup"><span data-stu-id="ca700-117">This folder must be open.</span></span>
    
 <span data-ttu-id="ca700-118">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="ca700-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="ca700-119">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca700-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ca700-120">Если в _лппрогресс_переДАЕТСЯ значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="ca700-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="ca700-121">Параметр _лппрогресс_ игнорируется, если не установлен флаг Мессаже_диалог в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ca700-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="ca700-122">_Лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="ca700-122">_lpProgress_</span></span>
  
> <span data-ttu-id="ca700-123">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca700-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ca700-124">Если в _лппрогресс_переДАЕТСЯ значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="ca700-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="ca700-125">Параметр _лппрогресс_ игнорируется, если не установлен флаг Мессаже_диалог в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ca700-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="ca700-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca700-126">_ulFlags_</span></span>
  
> <span data-ttu-id="ca700-127">возврата Битовая маска флагов, определяющих, как выполняется операция копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="ca700-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="ca700-128">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ca700-128">The following flags can be set:</span></span>
    
<span data-ttu-id="ca700-129">МЕССАЖЕ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="ca700-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="ca700-130">ЗаПрашивает отображение индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca700-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="ca700-131">МЕССАЖЕ_МОВЕ</span><span class="sxs-lookup"><span data-stu-id="ca700-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="ca700-132">Сообщения следует перемещать, а не копировать.</span><span class="sxs-lookup"><span data-stu-id="ca700-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="ca700-133">Если МЕССАЖЕ_МОВЕ не задано, сообщения копируются.</span><span class="sxs-lookup"><span data-stu-id="ca700-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca700-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca700-134">Return value</span></span>

<span data-ttu-id="ca700-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca700-135">S_OK</span></span> 
  
> <span data-ttu-id="ca700-136">Операция копирования или перемещения выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ca700-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="ca700-137">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="ca700-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ca700-138">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ca700-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ca700-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca700-139">Remarks</span></span>

<span data-ttu-id="ca700-140">Метод **имаписуппорт:: копимессажес** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ca700-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="ca700-141">Поставщики хранилищ сообщений могут вызывать **имаписуппорт:: копимессажес** в реализации [IMAPIFolder:: копимессажес](imapifolder-copymessages.md) для копирования или перемещения одного или нескольких сообщений из одной папки в другую.</span><span class="sxs-lookup"><span data-stu-id="ca700-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="ca700-142">В рамках вызова **имаписуппорт:: копимессажес** поставщик хранилища сообщений может указать, что MAPI должен отображать индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca700-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca700-143">См. также</span><span class="sxs-lookup"><span data-stu-id="ca700-143">See also</span></span>



[<span data-ttu-id="ca700-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ca700-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="ca700-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca700-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

