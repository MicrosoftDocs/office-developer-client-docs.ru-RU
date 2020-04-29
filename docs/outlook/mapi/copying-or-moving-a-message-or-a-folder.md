---
title: Копирование или перемещение сообщения или папки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Дата последнего изменения: 08 ноября 2011 г.'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413502"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="41e01-103">Копирование или перемещение сообщения или папки</span><span class="sxs-lookup"><span data-stu-id="41e01-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="41e01-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41e01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41e01-105">Для копирования или перемещения сообщения или папки клиент может использовать один из четырех способов:</span><span class="sxs-lookup"><span data-stu-id="41e01-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="41e01-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="41e01-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="41e01-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="41e01-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="41e01-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="41e01-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="41e01-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="41e01-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="41e01-110">Настроив соответствующие флаги и параметры, можно выполнить параметры **CopyTo** и **копипропс** , чтобы работать так же, как и **CopyFolder** , или **копимессажес**.</span><span class="sxs-lookup"><span data-stu-id="41e01-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="41e01-111">При выборе метода для вызова необходимо учитывать следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="41e01-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="41e01-112">Вы копируете или перемещаете папку или сообщение?</span><span class="sxs-lookup"><span data-stu-id="41e01-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="41e01-113">Насколько вы узнаете о папке или сообщении для перемещения или копирования?</span><span class="sxs-lookup"><span data-stu-id="41e01-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="41e01-114">Как будет перемещаться или копироваться количество свойств папки или сообщения?</span><span class="sxs-lookup"><span data-stu-id="41e01-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="41e01-115">Можно использовать методы **IMAPIProp** для копирования или перемещения папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="41e01-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="41e01-116">**IMAPIFolder:: копимессажес** работает только с сообщениями; **IMAPIFolder:: CopyFolder** работает только с папками.</span><span class="sxs-lookup"><span data-stu-id="41e01-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="41e01-117">В то время как при использовании методов **IMAPIFolder** не требуется знать о свойствах, поддерживаемых папкой или сообщением, для копирования или перемещения, необходимы некоторые знания для использования методов **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="41e01-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="41e01-118">С помощью **IMAPIProp:: копипропс**необходимо явным образом указать, какую папку или свойства сообщения необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="41e01-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="41e01-119">С **IMAPIProp:: CopyTo**, если вы не хотите копировать или перемещать все свойства, необходимо явным образом указать, какие из них следует исключить.</span><span class="sxs-lookup"><span data-stu-id="41e01-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="41e01-120">Дополнительные сведения об этих методах приведены в статье [Копирование свойств MAPI](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="41e01-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="41e01-121">Число копируемых или перемещаемых свойств может повлиять на ваше решение относительно используемого метода.</span><span class="sxs-lookup"><span data-stu-id="41e01-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="41e01-122">При копировании или перемещении нескольких сообщений вызовите метод **IMAPIFolder:: копимессажес**.</span><span class="sxs-lookup"><span data-stu-id="41e01-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="41e01-123">Альтернативный вариант — вызвать метод **IMAPIProp:: копипропс** , чтобы скопировать только свойство **PR_CONTAINER_CONTENTS** папки ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="41e01-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="41e01-124">В следующей процедуре показано, как использовать **копимессажес**.</span><span class="sxs-lookup"><span data-stu-id="41e01-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="41e01-125">Копирование или перемещение одного или нескольких сообщений</span><span class="sxs-lookup"><span data-stu-id="41e01-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="41e01-126">Поиск допустимых идентификаторов записей для исходной и конечной папок.</span><span class="sxs-lookup"><span data-stu-id="41e01-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="41e01-127">Откройте эти папки в режиме чтения и записи, вызвав один из [IMAPISession:: OpenEntry](imapisession-openentry.md) или [IMsgStore:: OpenEntry](imsgstore-openentry.md) и установив флаг MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="41e01-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="41e01-128">Убедитесь, что указатель интерфейса, возвращенный из **OpenEntry** , является указателем интерфейса **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="41e01-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="41e01-129">Если нет, приведите его к типу ЛПМАПИФОЛДЕР.</span><span class="sxs-lookup"><span data-stu-id="41e01-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="41e01-130">Создайте массив идентификаторов записей, представляющих одно или несколько сообщений, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="41e01-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="41e01-131">Call **IMAPIFolder:: копимессажес** со следующими установленными флагами:</span><span class="sxs-lookup"><span data-stu-id="41e01-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="41e01-132">MESSAGE_MOVE, если требуется выполнить операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="41e01-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="41e01-133">MESSAGE_DIALOG и передайте дескриптор окна в параметре _улуипарам_ , если необходимо, чтобы в папке отображался индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="41e01-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="41e01-134">Освободите указатели **IMAPIFolder** для исходной и конечной папок.</span><span class="sxs-lookup"><span data-stu-id="41e01-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="41e01-135">Если требуется скопировать полное содержимое папки в другую папку, вызовите метод **IMAPIFolder:: CopyFolder** или **IMAPIProp:: CopyTo** для исходной папки.</span><span class="sxs-lookup"><span data-stu-id="41e01-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="41e01-136">Чтобы скопировать несколько свойств папки, вызовите ее метод **IMAPIProp:: копипропс** .</span><span class="sxs-lookup"><span data-stu-id="41e01-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="41e01-137">Чтобы скопировать большую часть свойств папки, вызовите **IMAPIProp:: CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="41e01-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="41e01-138">Например, если нужно скопировать свойства **PR_DISPLAY_NAME** папки ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)), доступны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="41e01-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="41e01-139">Call **IMAPIFolder:: CopyFolder** , чтобы скопировать все свойства папки, а затем удалить ненужные из новой папки.</span><span class="sxs-lookup"><span data-stu-id="41e01-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="41e01-140">Вызовите функцию **CopyTo** и исключите все свойства папки, кроме **PR_DISPLAY_NAME** и **PR_COMMENT**.</span><span class="sxs-lookup"><span data-stu-id="41e01-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="41e01-141">Вызовите **копипропс**, передав **PR_DISPLAY_NAME** и **PR_COMMENT** в массив include.</span><span class="sxs-lookup"><span data-stu-id="41e01-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="41e01-142">В этом случае **копипропс** является лучшим вариантом, так как он предназначен для копирования небольшого набора свойств и является самым простым вызовом для реализации.</span><span class="sxs-lookup"><span data-stu-id="41e01-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="41e01-143">Чтобы скопировать или переместить только свойства папки, не включая сообщения, вызовите метод **IMAPIProp:: CopyTo** для папки и исключите следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="41e01-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="41e01-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41e01-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="41e01-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41e01-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="41e01-146">Методы Copy могут возвращать S_OK, указывающие общее успешное выполнение, MAPI_W_PARTIAL_COMPLETION, обозначающее частичное успешное выполнение, или ошибку.</span><span class="sxs-lookup"><span data-stu-id="41e01-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="41e01-147">Если возвращается MAPI_W_PARTIAL_COMPLETION, используйте макрос **HR_FAILED** для получения более подробных сообщений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="41e01-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="41e01-148">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="41e01-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="41e01-149">Если вы копируете сообщения из одного хранилища сообщений в другое, и Юникод не поддерживается обоими, то помните, что данные могут быть потеряны из-за преобразования кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="41e01-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="41e01-150">Как правило, вы не можете определить, поддерживает ли хранилище сообщений один или оба формата, что невозможно определить, нужно ли копировать свойства текста как строки ASCII или как строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="41e01-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="41e01-151">Если вы поддерживаете Юникод, попробуйте выполнить копирование в кодировке Юникод; Если произойдет сбой со значением ошибки MAPI_E_BAD_CHARWIDTH, следует прибегнуть к текстовому символу ASCII.</span><span class="sxs-lookup"><span data-stu-id="41e01-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

