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
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412886"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="88e72-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="88e72-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="88e72-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88e72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88e72-105">Определяет, может ли форма обрабатывать собственные конфликты сообщений.</span><span class="sxs-lookup"><span data-stu-id="88e72-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="88e72-106">Сообщение конфликтует, если оно было одновременно изменено более чем одним пользователем.</span><span class="sxs-lookup"><span data-stu-id="88e72-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="88e72-107">Это может произойти с сообщениями в общедоступных папках.</span><span class="sxs-lookup"><span data-stu-id="88e72-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="88e72-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="88e72-108">Parameters</span></span>

 <span data-ttu-id="88e72-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="88e72-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="88e72-110">[in] Указатель на битовуюmask флагов, скопированную из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, которое указывает текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="88e72-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="88e72-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="88e72-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="88e72-112">[in] Битовая почта клиентских или определяемых поставщиком флагов, скопированная из свойства **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, которая предоставляет дополнительные сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="88e72-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="88e72-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="88e72-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="88e72-114">[in] Строка, которая именует класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="88e72-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="88e72-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="88e72-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="88e72-116">[in] Указатель на папку, содержаную сообщение.</span><span class="sxs-lookup"><span data-stu-id="88e72-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="88e72-117">Параметр  _pFolderFocus_ может иметь NULL, если такая папка не существует (например, если сообщение внедрено в другое сообщение).</span><span class="sxs-lookup"><span data-stu-id="88e72-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="88e72-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88e72-118">Return value</span></span>

<span data-ttu-id="88e72-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="88e72-119">S_OK</span></span> 
  
> <span data-ttu-id="88e72-120">Форма не обрабатывает собственные конфликты сообщений.</span><span class="sxs-lookup"><span data-stu-id="88e72-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="88e72-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="88e72-121">S_FALSE</span></span> 
  
> <span data-ttu-id="88e72-122">Форма обрабатывает собственные конфликты сообщений или сообщение, сведения о котором были переданы, не конфликтуют.</span><span class="sxs-lookup"><span data-stu-id="88e72-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88e72-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="88e72-123">Remarks</span></span>

<span data-ttu-id="88e72-124">Посетители форм звонят **методу IMAPIFormMgr::IsInConflict,** чтобы определить, не обрабатывает ли конкретная форма собственные конфликты сообщений.</span><span class="sxs-lookup"><span data-stu-id="88e72-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="88e72-125">**IsInConflict** проверяет битовыеmasks в  _параметрах ulMessageFlags_ и  _ulMessageStatus_ на наличие флага конфликта.</span><span class="sxs-lookup"><span data-stu-id="88e72-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="88e72-126">Если установлен флаг конфликта, **IsInConflict** разрешает класс сообщения, переданный в  _параметре szMessageClass,_ и возвращает S_OK, если форма не обрабатывает собственные конфликты.</span><span class="sxs-lookup"><span data-stu-id="88e72-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="88e72-127">**IsInConflict** возвращает S_FALSE, если форма обрабатывает собственные конфликты.</span><span class="sxs-lookup"><span data-stu-id="88e72-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="88e72-128">Форма, не обрабатывающая собственные конфликты, должна быть открыта с помощью метода [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) и не может повторно использовать существующий объект формы.</span><span class="sxs-lookup"><span data-stu-id="88e72-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="88e72-129">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="88e72-129">Notes to callers</span></span>

<span data-ttu-id="88e72-130">Клиентские приложения обычно должны иметь дело с конфликтами, когда приложения перемещаются из одного сообщения в следующее или предыдущее сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="88e72-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="88e72-131">Если сообщение конфликтует, но сервер форм для этого сообщения может обработать конфликты, клиентские приложения должны выполнить свой обычный код для отображения следующего или предыдущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="88e72-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="88e72-132">Если сервер форм не может обработать конфликты, клиентские приложения должны продолжать работу так, как если бы он не знал о классе сообщения следующего или предыдущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="88e72-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88e72-133">См. также</span><span class="sxs-lookup"><span data-stu-id="88e72-133">See also</span></span>



[<span data-ttu-id="88e72-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="88e72-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="88e72-135">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="88e72-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="88e72-136">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="88e72-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="88e72-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="88e72-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

