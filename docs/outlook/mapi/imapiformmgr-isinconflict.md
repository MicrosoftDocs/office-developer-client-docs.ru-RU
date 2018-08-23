---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 329771bf79e30f07c9de0a311aa2a836ca507c38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580035"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="8eefe-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="8eefe-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="8eefe-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8eefe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8eefe-105">Определяет ли формы можно обработать собственный конфликтов сообщения.</span><span class="sxs-lookup"><span data-stu-id="8eefe-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="8eefe-106">Сообщение находится в конфликт, если она была отредактирована одновременно с более одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="8eefe-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="8eefe-107">Это может произойти в сообщения в общих папках.</span><span class="sxs-lookup"><span data-stu-id="8eefe-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="8eefe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8eefe-108">Parameters</span></span>

 <span data-ttu-id="8eefe-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="8eefe-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="8eefe-110">[in] Указатель на битовой маски флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщение, указывающее текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="8eefe-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="8eefe-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="8eefe-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="8eefe-112">[in] Битовая маска флагов клиента или поставщика, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, которое предоставляет дополнительные сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="8eefe-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="8eefe-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="8eefe-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="8eefe-114">[in] Строка, имена класс сообщения сообщения.</span><span class="sxs-lookup"><span data-stu-id="8eefe-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="8eefe-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="8eefe-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="8eefe-116">[in] Указатель на папку, содержащую сообщение.</span><span class="sxs-lookup"><span data-stu-id="8eefe-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="8eefe-117">Параметр _pFolderFocus_ может быть NULL, если такая папка не существует (например, если сообщение встроена в другое сообщение).</span><span class="sxs-lookup"><span data-stu-id="8eefe-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8eefe-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8eefe-118">Return value</span></span>

<span data-ttu-id="8eefe-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="8eefe-119">S_OK</span></span> 
  
> <span data-ttu-id="8eefe-120">Форма не обрабатывает собственный конфликтов сообщения.</span><span class="sxs-lookup"><span data-stu-id="8eefe-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="8eefe-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="8eefe-121">S_FALSE</span></span> 
  
> <span data-ttu-id="8eefe-122">Форма обрабатывает собственный конфликтов сообщения или сообщения, для которого был передан сведения не конфликта.</span><span class="sxs-lookup"><span data-stu-id="8eefe-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8eefe-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="8eefe-123">Remarks</span></span>

<span data-ttu-id="8eefe-124">Средства просмотра форм вызовите метод **IMAPIFormMgr::IsInConflict** для обнаружения ли определенной формы не обрабатывает собственный конфликтов сообщения.</span><span class="sxs-lookup"><span data-stu-id="8eefe-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="8eefe-125">**IsInConflict** проверяет битовой маски в параметрах _ulMessageFlags_ и _ulMessageStatus_ на наличие конфликта флаг.</span><span class="sxs-lookup"><span data-stu-id="8eefe-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="8eefe-126">Если значение флага конфликта, **IsInConflict** разрешает класс сообщения, переданной в параметре _szMessageClass_ и возвращает значение S_OK, если форма не обрабатывает собственный конфликтов.</span><span class="sxs-lookup"><span data-stu-id="8eefe-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="8eefe-127">**IsInConflict** возвращает S_FALSE, если форма обрабатывает собственный конфликтов.</span><span class="sxs-lookup"><span data-stu-id="8eefe-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="8eefe-128">Формы, которая не обрабатывает собственный конфликтов необходимо открыть с помощью метода [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) и не может использовать существующий объект формы.</span><span class="sxs-lookup"><span data-stu-id="8eefe-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8eefe-129">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8eefe-129">Notes to callers</span></span>

<span data-ttu-id="8eefe-130">Клиентские приложения обычно иметь дело с конфликтами при перемещения приложений из одного сообщения на следующий или предыдущий сообщения в папке.</span><span class="sxs-lookup"><span data-stu-id="8eefe-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="8eefe-131">Если сообщение находится в конфликт, но сервер формы для этого сообщения можно обрабатывать конфликты, клиентское приложение должно выполнить его обычным код для отображения сообщения следующий или предыдущий.</span><span class="sxs-lookup"><span data-stu-id="8eefe-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="8eefe-132">Если сервер формы не может обработать конфликтов, клиентское приложение следует перейти, как если бы он был знают о класса сообщений для сообщений следующий или предыдущий.</span><span class="sxs-lookup"><span data-stu-id="8eefe-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8eefe-133">См. также</span><span class="sxs-lookup"><span data-stu-id="8eefe-133">See also</span></span>



[<span data-ttu-id="8eefe-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="8eefe-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="8eefe-135">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="8eefe-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="8eefe-136">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="8eefe-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="8eefe-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8eefe-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

