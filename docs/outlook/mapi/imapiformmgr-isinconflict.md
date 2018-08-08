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
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808927"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="85832-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="85832-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="85832-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85832-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85832-105">Определяет ли формы можно обработать собственный конфликтов сообщения.</span><span class="sxs-lookup"><span data-stu-id="85832-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="85832-106">Сообщение находится в конфликт, если она была отредактирована одновременно с более одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="85832-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="85832-107">Это может произойти в сообщения в общих папках.</span><span class="sxs-lookup"><span data-stu-id="85832-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="85832-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85832-108">Parameters</span></span>

 <span data-ttu-id="85832-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="85832-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="85832-110">[in] Указатель на битовой маски флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщение, указывающее текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="85832-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="85832-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="85832-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="85832-112">[in] Битовая маска флагов клиента или поставщика, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, которое предоставляет дополнительные сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="85832-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="85832-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="85832-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="85832-114">[in] Строка, имена класс сообщения сообщения.</span><span class="sxs-lookup"><span data-stu-id="85832-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="85832-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="85832-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="85832-116">[in] Указатель на папку, содержащую сообщение.</span><span class="sxs-lookup"><span data-stu-id="85832-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="85832-117">Параметр _pFolderFocus_ может быть NULL, если такая папка не существует (например, если сообщение встроена в другое сообщение).</span><span class="sxs-lookup"><span data-stu-id="85832-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85832-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="85832-118">Return value</span></span>

<span data-ttu-id="85832-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="85832-119">S_OK</span></span> 
  
> <span data-ttu-id="85832-120">Форма не обрабатывает собственный конфликтов сообщения.</span><span class="sxs-lookup"><span data-stu-id="85832-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="85832-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="85832-121">S_FALSE</span></span> 
  
> <span data-ttu-id="85832-122">Форма обрабатывает собственный конфликтов сообщения или сообщения, для которого был передан сведения не конфликта.</span><span class="sxs-lookup"><span data-stu-id="85832-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85832-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="85832-123">Remarks</span></span>

<span data-ttu-id="85832-124">Средства просмотра форм вызовите метод **IMAPIFormMgr::IsInConflict** для обнаружения ли определенной формы не обрабатывает собственный конфликтов сообщения.</span><span class="sxs-lookup"><span data-stu-id="85832-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="85832-125">**IsInConflict** проверяет битовой маски в параметрах _ulMessageFlags_ и _ulMessageStatus_ на наличие конфликта флаг.</span><span class="sxs-lookup"><span data-stu-id="85832-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="85832-126">Если значение флага конфликта, **IsInConflict** разрешает класс сообщения, переданной в параметре _szMessageClass_ и возвращает значение S_OK, если форма не обрабатывает собственный конфликтов.</span><span class="sxs-lookup"><span data-stu-id="85832-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="85832-127">**IsInConflict** возвращает S_FALSE, если форма обрабатывает собственный конфликтов.</span><span class="sxs-lookup"><span data-stu-id="85832-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="85832-128">Формы, которая не обрабатывает собственный конфликтов необходимо открыть с помощью метода [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) и не может использовать существующий объект формы.</span><span class="sxs-lookup"><span data-stu-id="85832-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="85832-129">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="85832-129">Notes to callers</span></span>

<span data-ttu-id="85832-130">Клиентские приложения обычно иметь дело с конфликтами при перемещения приложений из одного сообщения на следующий или предыдущий сообщения в папке.</span><span class="sxs-lookup"><span data-stu-id="85832-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="85832-131">Если сообщение находится в конфликт, но сервер формы для этого сообщения можно обрабатывать конфликты, клиентское приложение должно выполнить его обычным код для отображения сообщения следующий или предыдущий.</span><span class="sxs-lookup"><span data-stu-id="85832-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="85832-132">Если сервер формы не может обработать конфликтов, клиентское приложение следует перейти, как если бы он был знают о класса сообщений для сообщений следующий или предыдущий.</span><span class="sxs-lookup"><span data-stu-id="85832-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85832-133">См. также</span><span class="sxs-lookup"><span data-stu-id="85832-133">See also</span></span>



[<span data-ttu-id="85832-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="85832-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="85832-135">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="85832-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="85832-136">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="85832-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="85832-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85832-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

