---
title: Имапиформмгрисинконфликт
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
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="e6dc0-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="e6dc0-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="e6dc0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6dc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6dc0-105">Определяет, может ли форма обрабатывать свои собственные конфликты сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="e6dc0-106">Сообщение конфликтует с другим пользователем, если оно было одновременно изменено несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="e6dc0-107">Это может произойти в сообщениях в общедоступных папках.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="e6dc0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6dc0-108">Parameters</span></span>

 <span data-ttu-id="e6dc0-109">_Улмессажефлагс_</span><span class="sxs-lookup"><span data-stu-id="e6dc0-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="e6dc0-110">возврата Указатель на битовую маску флагов, скопированных из свойства **пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения, которое показывает текущее состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="e6dc0-111">_Улмессажестатус_</span><span class="sxs-lookup"><span data-stu-id="e6dc0-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="e6dc0-112">возврата Битовая маска заданных клиентом или поставщиками флагов, скопированных из свойства **пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, которое предоставляет дополнительные сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="e6dc0-113">_Сзмессажекласс_</span><span class="sxs-lookup"><span data-stu-id="e6dc0-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="e6dc0-114">возврата Строка, которая присваивает имя классу сообщений сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="e6dc0-115">_Пфолдерфокус_</span><span class="sxs-lookup"><span data-stu-id="e6dc0-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="e6dc0-116">возврата Указатель на папку, в которой находится сообщение.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="e6dc0-117">Параметр _пфолдерфокус_ может иметь значение null, если такая папка не существует (например, если сообщение внедрено в другое сообщение).</span><span class="sxs-lookup"><span data-stu-id="e6dc0-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e6dc0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6dc0-118">Return value</span></span>

<span data-ttu-id="e6dc0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6dc0-119">S_OK</span></span> 
  
> <span data-ttu-id="e6dc0-120">Форма не обрабатывает свои собственные конфликты сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="e6dc0-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e6dc0-121">S_FALSE</span></span> 
  
> <span data-ttu-id="e6dc0-122">Форма обрабатывает свои собственные конфликты сообщений, или сообщение, для которого были переданы сведения, не конфликтует.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6dc0-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="e6dc0-123">Remarks</span></span>

<span data-ttu-id="e6dc0-124">Средства просмотра форм вызывают метод **имапиформмгр:: исинконфликт** , чтобы определить, не обрабатывает ли определенная форма свои собственные конфликты сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="e6dc0-125">**Исинконфликт** проверяет побитовые маски в параметрах _улмессажефлагс_ и _улмессажестатус_ на наличие флага конфликта.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="e6dc0-126">Если установлен флаг конфликта, **исинконфликт** разрешает класс сообщений, переданный в параметре _сзмессажекласс_ , и возвращает значение S_OK, если форма не обрабатывает свои собственные конфликты.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="e6dc0-127">**Исинконфликт** возвращает S_FALSE, если форма обрабатывает свои собственные конфликты.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="e6dc0-128">Форма, которая не обрабатывает свои собственные конфликты, должна быть открыта с помощью метода [имапиформмгр:: лоадформ](imapiformmgr-loadform.md) и не может повторно использовать существующий объект Form.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e6dc0-129">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e6dc0-129">Notes to callers</span></span>

<span data-ttu-id="e6dc0-130">Как правило, клиентским приложениям приходится обращаться к конфликтам при перемещении приложений из одного сообщения в следующее или предыдущее сообщение в папке.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="e6dc0-131">Если сообщение конфликтует с, но сервер форм для этого сообщения может обрабатывать конфликты, клиентское приложение должно выполнить обычный код для отображения следующего или предыдущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="e6dc0-132">Если сервер форм не может обрабатывать конфликты, клиентское приложение должно продолжаться так, как если бы оно было неосведомленным о классе сообщения следующего или предыдущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6dc0-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6dc0-133">См. также</span><span class="sxs-lookup"><span data-stu-id="e6dc0-133">See also</span></span>



[<span data-ttu-id="e6dc0-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="e6dc0-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="e6dc0-135">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="e6dc0-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="e6dc0-136">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="e6dc0-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="e6dc0-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6dc0-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

