---
title: Копирование или перемещение сообщения или папки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413502"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="03d3b-103">Копирование или перемещение сообщения или папки</span><span class="sxs-lookup"><span data-stu-id="03d3b-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="03d3b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03d3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03d3b-105">Клиент может использовать один из четырех методов для копирования или перемещения сообщения или папки:</span><span class="sxs-lookup"><span data-stu-id="03d3b-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="03d3b-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="03d3b-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="03d3b-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="03d3b-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="03d3b-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="03d3b-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="03d3b-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="03d3b-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="03d3b-110">Установив соответствующие флаги и параметры, **CopyTo** и **CopyProps** можно сделать так же, как **CopyFolder** или **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="03d3b-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="03d3b-111">При выборе метода вызова следует учитывать следующие проблемы.</span><span class="sxs-lookup"><span data-stu-id="03d3b-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="03d3b-112">Копируете или перемещаете папку или сообщение?</span><span class="sxs-lookup"><span data-stu-id="03d3b-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="03d3b-113">Сколько вы знаете о папке или сообщении, которые будут перемещены или скопированы?</span><span class="sxs-lookup"><span data-stu-id="03d3b-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="03d3b-114">Сколько свойств папки или сообщения будет перемещено или скопировано?</span><span class="sxs-lookup"><span data-stu-id="03d3b-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="03d3b-115">С помощью **методов IMAPIProp** можно скопировать или переместить папку или сообщение.</span><span class="sxs-lookup"><span data-stu-id="03d3b-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="03d3b-116">**IMAPIFolder::CopyMessages работает** только с сообщениями; **IMAPIFolder::CopyFolder** работает только с папками.</span><span class="sxs-lookup"><span data-stu-id="03d3b-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="03d3b-117">В то время как использование методов **IMAPIFolder** не требует каких-либо знаний о свойствах, поддерживаемых папкой или сообщением для копирования или перемещений, необходимо иметь некоторые знания для использования методов **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="03d3b-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="03d3b-118">С **помощью IMAPIProp::CopyProps** необходимо четко указать, какие из свойств папки или сообщений необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="03d3b-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="03d3b-119">С **IMAPIProp::CopyTo**, если вы не хотите скопировать или переместить все свойства, необходимо четко указать, какие из них следует исключить.</span><span class="sxs-lookup"><span data-stu-id="03d3b-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="03d3b-120">Дополнительные сведения об этих методах см. в дополнительных сведениях [о копировании свойств MAPI.](copying-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="03d3b-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="03d3b-121">Количество свойств, которые будут скопированы или перемещены, может повлиять на ваше решение о том, какой метод использовать.</span><span class="sxs-lookup"><span data-stu-id="03d3b-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="03d3b-122">Если вы копируете или перемещает несколько сообщений, позвоните **в IMAPIFolder::CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="03d3b-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="03d3b-123">Альтернативный выбор — вызвать **IMAPIProp::CopyProps,** **чтобы скопировать** только свойство [PR_CONTAINER_CONTENTS (PidTagContainerContents).](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="03d3b-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="03d3b-124">Следующая процедура показывает, как использовать **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="03d3b-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="03d3b-125">Копирование или перемещение одного или более сообщений</span><span class="sxs-lookup"><span data-stu-id="03d3b-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="03d3b-126">Найдите допустимые идентификаторы записи для исходных и назначений папок.</span><span class="sxs-lookup"><span data-stu-id="03d3b-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="03d3b-127">Откройте эти папки в режиме чтения и записи, позвонив [в IMAPISession::OpenEntry](imapisession-openentry.md) или [IMsgStore::OpenEntry](imsgstore-openentry.md) и задав флаг MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="03d3b-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="03d3b-128">Убедитесь, что указатель интерфейса, возвращенный **из OpenEntry,** является **указателем интерфейса IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="03d3b-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="03d3b-129">Если нет, отведите его в тип LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="03d3b-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="03d3b-130">Создайте массив идентификаторов записей, представляющих одно или несколько сообщений, которые будут скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="03d3b-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="03d3b-131">Вызов **IMAPIFolder::CopyMessages со** следующим набором флагов:</span><span class="sxs-lookup"><span data-stu-id="03d3b-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="03d3b-132">MESSAGE_MOVE, если вы хотите выполнить операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="03d3b-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="03d3b-133">MESSAGE_DIALOG и передай ручку окна в  _параметре ulUIParam,_ если нужно, чтобы в папке был индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="03d3b-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="03d3b-134">**Отпустите указатели IMAPIFolder** для исходных папок и папок назначения.</span><span class="sxs-lookup"><span data-stu-id="03d3b-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="03d3b-135">Если вы хотите скопировать полное содержимое папки в другую папку, позвоните по методу **IMAPIFolder::CopyFolder** или **IMAPIProp::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="03d3b-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="03d3b-136">Чтобы скопировать несколько свойств папки, позвоните по методу **IMAPIProp::CopyProps.**</span><span class="sxs-lookup"><span data-stu-id="03d3b-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="03d3b-137">Чтобы скопировать большинство свойств папки, позвоните **в IMAPIProp::CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="03d3b-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="03d3b-138">Например, если вы хотите скопировать свойства  PR_DISPLAY_NAME [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и **PR_COMMENT** [(PidTagComment),](pidtagcomment-canonical-property.md)у вас есть следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="03d3b-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="03d3b-139">Позвоните **в IMAPIFolder::CopyFolder,** чтобы скопировать все свойства папки, а затем удалить нежелательные из новой папки.</span><span class="sxs-lookup"><span data-stu-id="03d3b-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="03d3b-140">Вызов **CopyTo** и исключить все свойства папки, за исключением PR_DISPLAY_NAME **и PR_COMMENT**. </span><span class="sxs-lookup"><span data-stu-id="03d3b-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="03d3b-141">Вызов **CopyProps,** **PR_DISPLAY_NAME** и **PR_COMMENT** в массиве включить.</span><span class="sxs-lookup"><span data-stu-id="03d3b-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="03d3b-142">В этом случае **CopyProps** — это лучший выбор, так как он предназначен для копирования небольшого набора свойств и является самым простым вызовом для реализации.</span><span class="sxs-lookup"><span data-stu-id="03d3b-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="03d3b-143">Чтобы скопировать или переместить только свойства папок, не включая сообщения, позвоните по методу **IMAPIProp::CopyTo** и исключите следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="03d3b-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="03d3b-144">**PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="03d3b-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="03d3b-145">**PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="03d3b-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="03d3b-146">Методы копирования могут S_OK, что указывает на общий успех, MAPI_W_PARTIAL_COMPLETION, что указывает на частичный успех или ошибку.</span><span class="sxs-lookup"><span data-stu-id="03d3b-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="03d3b-147">Если MAPI_W_PARTIAL_COMPLETION возвращается, **используйте макрос HR_FAILED,** чтобы получить доступ к более конкретной ошибке.</span><span class="sxs-lookup"><span data-stu-id="03d3b-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="03d3b-148">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="03d3b-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="03d3b-149">Если вы скопируете сообщения из одного магазина сообщений в другой и Юникод не поддерживается обеими сторонами, следует помнить, что информация может быть потеряна из-за преобразования страницы кода.</span><span class="sxs-lookup"><span data-stu-id="03d3b-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="03d3b-150">Обычно вы не можете знать, поддерживают ли хранилища сообщений один или оба формата, из-за чего невозможно определить, следует ли копировать свойства текста как строки ASCII или строки Юникод.</span><span class="sxs-lookup"><span data-stu-id="03d3b-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="03d3b-151">Если вы поддерживаете Юникод, попробуйте выполнить копию Юникод; если она не справилась со значением ошибки MAPI_E_BAD_CHARWIDTH, прибегли к ASCII.</span><span class="sxs-lookup"><span data-stu-id="03d3b-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

