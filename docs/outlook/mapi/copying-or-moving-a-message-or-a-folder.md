---
title: Копирование и перемещение папки или сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: 26fe135da93e0f5f94d9f7d264453b74f97a518b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808233"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="1b577-103">Копирование и перемещение папки или сообщения</span><span class="sxs-lookup"><span data-stu-id="1b577-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="1b577-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b577-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b577-105">Клиент может использовать один из четырех методов для копирования или перемещения сообщения или папки:</span><span class="sxs-lookup"><span data-stu-id="1b577-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="1b577-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="1b577-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="1b577-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1b577-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="1b577-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="1b577-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="1b577-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="1b577-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="1b577-110">Задав соответствующие флаги и параметры, **CopyTo** и **CopyProps** может быть установлено работают так же, как **CopyFolder** или **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="1b577-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="1b577-111">При выборе метод, вызываемый необходимо учитывайте следующее:</span><span class="sxs-lookup"><span data-stu-id="1b577-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="1b577-112">Копирование или перемещение папки или сообщение?</span><span class="sxs-lookup"><span data-stu-id="1b577-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="1b577-113">Сколько вы знаете о папку или сообщение для перемещения или копирования?</span><span class="sxs-lookup"><span data-stu-id="1b577-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="1b577-114">Сколько папки или свойства сообщения будут перемещены или скопированы?</span><span class="sxs-lookup"><span data-stu-id="1b577-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="1b577-115">Скопируйте или переместите папку или сообщение воспользуйтесь методом **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="1b577-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="1b577-116">**IMAPIFolder::CopyMessages** для работы с сообщений **IMAPIFolder::CopyFolder** для работы с только папки.</span><span class="sxs-lookup"><span data-stu-id="1b577-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="1b577-117">В то время как с помощью методов **IMAPIFolder** не требует знания свойства, поддерживаемые в папку или на сообщение, чтобы скопировать или переместить, необходимо иметь некоторые базы знаний, чтобы использовать методы **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="1b577-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="1b577-118">С помощью **IMAPIProp::CopyProps**необходимо явно указать, какие свойства папки или сообщения, которые нужно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="1b577-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="1b577-119">С помощью **IMAPIProp::CopyTo**Если не требуется скопировать или переместить все свойства, необходимо явно задать какие из них следует исключить.</span><span class="sxs-lookup"><span data-stu-id="1b577-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="1b577-120">Дополнительные сведения об этих методов можно [Копирование свойств MAPI](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1b577-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="1b577-121">Число свойств можно скопировать или переместить могут повлиять на ваше решение о том, какой метод следует использовать.</span><span class="sxs-lookup"><span data-stu-id="1b577-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="1b577-122">Если копирование или перемещение нескольких сообщений, вызовите **IMAPIFolder::CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="1b577-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="1b577-123">Альтернативный вариант — вызов **IMAPIProp::CopyProps** для копирования только свойства папки **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1b577-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="1b577-124">Следующей процедуре показано, как использовать **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="1b577-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="1b577-125">Копирование или перемещение одно или несколько сообщений</span><span class="sxs-lookup"><span data-stu-id="1b577-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="1b577-126">Найдите идентификаторы записей для исходной и конечной папки.</span><span class="sxs-lookup"><span data-stu-id="1b577-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="1b577-127">Откройте эти папки в режиме чтения и записи, вызов [IMAPISession::OpenEntry](imapisession-openentry.md) или [IMsgStore::OpenEntry](imsgstore-openentry.md) и установка флага MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="1b577-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="1b577-128">Убедитесь, что указатель интерфейса, возвращенный из **OpenEntry** указатель интерфейса **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="1b577-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="1b577-129">В противном случае привести к типу LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="1b577-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="1b577-130">Создайте массив идентификаторов запись представляет одно или несколько сообщений можно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="1b577-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="1b577-131">Вызовите **IMAPIFolder::CopyMessages** с помощью следующей последовательности флаги:</span><span class="sxs-lookup"><span data-stu-id="1b577-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="1b577-132">MESSAGE_MOVE, если требуется выполнить операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="1b577-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="1b577-133">MESSAGE_DIALOG и передайте окно обрабатывать с помощью параметра _ulUIParam_ папка для отображения индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1b577-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="1b577-134">Освобождение указатели **IMAPIFolder** для исходной и конечной папки.</span><span class="sxs-lookup"><span data-stu-id="1b577-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="1b577-135">Если требуется скопировать все содержимое папки в другую папку, вызовите метод **IMAPIFolder::CopyFolder** или **IMAPIProp::CopyTo** исходной папки.</span><span class="sxs-lookup"><span data-stu-id="1b577-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="1b577-136">Чтобы скопировать несколько свойств папки, вызове метода **IMAPIProp::CopyProps** .</span><span class="sxs-lookup"><span data-stu-id="1b577-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="1b577-137">Чтобы скопировать большая часть свойств папки, вызовите **IMAPIProp::CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="1b577-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="1b577-138">Например если требуется скопировать свойства **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) и **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) папки, у вас есть следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1b577-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="1b577-139">Вызовите **IMAPIFolder::CopyFolder** , чтобы скопировать все свойства папки, а затем удалить ненужные из них в новую папку.</span><span class="sxs-lookup"><span data-stu-id="1b577-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="1b577-140">Вызовите **CopyTo** и исключить все свойства папки кроме **PR_DISPLAY_NAME** и **PR_COMMENT**.</span><span class="sxs-lookup"><span data-stu-id="1b577-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="1b577-141">Вызовите **CopyProps**, передав **PR_DISPLAY_NAME** и **PR_COMMENT** в массиве include.</span><span class="sxs-lookup"><span data-stu-id="1b577-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="1b577-142">В этом случае **CopyProps** является оптимальным выбором, так как он должен использоваться для копирования небольшой набор свойств и это самый простой вызов для реализации.</span><span class="sxs-lookup"><span data-stu-id="1b577-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="1b577-143">Чтобы скопировать или переместить только свойства папки, не включая сообщения, вызовите метод **IMAPIProp::CopyTo** папки и исключить следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="1b577-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="1b577-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1b577-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="1b577-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1b577-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="1b577-146">Методы копирования может возвращать значение S_OK, общее успешно, MAPI_W_PARTIAL_COMPLETION, указывающего на то, указывающее, частичный успех или ошибка.</span><span class="sxs-lookup"><span data-stu-id="1b577-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="1b577-147">Если MAPI_W_PARTIAL_COMPLETION возвращается, используйте макрос **HR_FAILED** для доступа к более конкретной ошибки.</span><span class="sxs-lookup"><span data-stu-id="1b577-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="1b577-148">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1b577-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="1b577-149">Если копирование сообщений из одного хранилища в другое и Юникод не поддерживается в обоих, обратите внимание, что данные могут быть потеряны из-за преобразования кода страницы.</span><span class="sxs-lookup"><span data-stu-id="1b577-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="1b577-150">Обычно нельзя известно, если хранилищ сообщений поддерживает форматы один или оба, делая невозможным определить, нужно ли скопировать текст свойства как строки ASCII или Юникод.</span><span class="sxs-lookup"><span data-stu-id="1b577-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="1b577-151">Если вы поддерживаете Юникод, попробуйте выполнить копия Юникод. в случае сбоя со значением ошибки MAPI_E_BAD_CHARWIDTH прибегать к ASCII.</span><span class="sxs-lookup"><span data-stu-id="1b577-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

