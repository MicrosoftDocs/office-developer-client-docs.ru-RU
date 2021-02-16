---
title: Копирование или перемещение сообщения или папки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413502"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="4a79a-103">Копирование или перемещение сообщения или папки</span><span class="sxs-lookup"><span data-stu-id="4a79a-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="4a79a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a79a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a79a-105">Клиент может использовать один из четырех методов копирования или перемещения сообщения или папки:</span><span class="sxs-lookup"><span data-stu-id="4a79a-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="4a79a-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="4a79a-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="4a79a-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="4a79a-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="4a79a-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="4a79a-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="4a79a-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="4a79a-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="4a79a-110">Установив соответствующие флаги и параметры, **CopyTo** и **CopyProps** можно сделать так же, как **CopyFolder** или **CopyMessages.**</span><span class="sxs-lookup"><span data-stu-id="4a79a-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="4a79a-111">При выборе метода вызова учитывайте следующие проблемы:</span><span class="sxs-lookup"><span data-stu-id="4a79a-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="4a79a-112">Копируете или перемещаете папку или сообщение?</span><span class="sxs-lookup"><span data-stu-id="4a79a-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="4a79a-113">Сколько вы знаете о папке или сообщении, которые необходимо скопировать?</span><span class="sxs-lookup"><span data-stu-id="4a79a-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="4a79a-114">Сколько свойств папки или сообщения будет перемещено или скопировано?</span><span class="sxs-lookup"><span data-stu-id="4a79a-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="4a79a-115">Методы **IMAPIProp** можно использовать для копирования или перемещения папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="4a79a-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="4a79a-116">**IMAPIFolder::CopyMessages** работает только с сообщениями; **IMAPIFolder::CopyFolder работает** только с папками.</span><span class="sxs-lookup"><span data-stu-id="4a79a-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="4a79a-117">В то время как для использования методов **IMAPIFolder** не требуется знание свойств, поддерживаемых папкой или сообщением для копирования или перемещений, для использования методов **IMAPIProp** необходимы некоторые знания.</span><span class="sxs-lookup"><span data-stu-id="4a79a-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="4a79a-118">С **помощью IMAPIProp::CopyProps** необходимо иметь возможность явным образом указать, какое из свойств папки или сообщения необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="4a79a-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="4a79a-119">С **помощью IMAPIProp::CopyTo**, если вы не хотите копировать или перемещать все свойства, необходимо явно указать, какие из них следует исключить.</span><span class="sxs-lookup"><span data-stu-id="4a79a-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="4a79a-120">Дополнительные сведения об этих методах см. в сведениях [о копировании свойств MAPI.](copying-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="4a79a-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="4a79a-121">Количество скопирований или перемещений свойств может повлиять на принятие решения о том, какой метод использовать.</span><span class="sxs-lookup"><span data-stu-id="4a79a-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="4a79a-122">При копировании или перемещении нескольких сообщений вызовите **IMAPIFolder::CopyMessages.**</span><span class="sxs-lookup"><span data-stu-id="4a79a-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="4a79a-123">Альтернативным вариантом является вызов **IMAPIProp::CopyProps** для копирования только свойства **PR_CONTAINER_CONTENTS** папки ([PidTagContainerContents).](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4a79a-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="4a79a-124">В следующей процедуре показано, как **использовать CopyMessages.**</span><span class="sxs-lookup"><span data-stu-id="4a79a-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="4a79a-125">Копирование или перемещение одного или более сообщений</span><span class="sxs-lookup"><span data-stu-id="4a79a-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="4a79a-126">Найдите допустимые идентификаторы записей для исходных и папок назначения.</span><span class="sxs-lookup"><span data-stu-id="4a79a-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="4a79a-127">Откройте эти папки в режиме чтения и записи, вызывая [IMAPISession::OpenEntry](imapisession-openentry.md) или [IMsgStore::OpenEntry](imsgstore-openentry.md) и устанавливая флаг MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="4a79a-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="4a79a-128">Убедитесь, что указатель интерфейса, возвращаемой **из OpenEntry,** является указателем интерфейса **IMAPIFolder.**</span><span class="sxs-lookup"><span data-stu-id="4a79a-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="4a79a-129">Если нет, приведите его к типу LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="4a79a-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="4a79a-130">Создайте массив идентификаторов записей, представляющих одно или несколько сообщений для копирования или перемещений.</span><span class="sxs-lookup"><span data-stu-id="4a79a-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="4a79a-131">Вызовите **IMAPIFolder::CopyMessages** со следующими установленными флагами:</span><span class="sxs-lookup"><span data-stu-id="4a79a-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="4a79a-132">MESSAGE_MOVE, если вы хотите выполнить операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="4a79a-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="4a79a-133">MESSAGE_DIALOG и передать окне в  _параметре ulUIParam,_ если необходимо, чтобы в папке был индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4a79a-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="4a79a-134">**Отпустите указатели IMAPIFolder** для исходных и папок назначения.</span><span class="sxs-lookup"><span data-stu-id="4a79a-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="4a79a-135">Чтобы скопировать все содержимое папки в другую папку, вызовите метод **IMAPIFolder::CopyFolder** или **IMAPIProp::CopyTo** в папке источника.</span><span class="sxs-lookup"><span data-stu-id="4a79a-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="4a79a-136">Чтобы скопировать несколько свойств папки, вызовите метод **IMAPIProp::CopyProps.**</span><span class="sxs-lookup"><span data-stu-id="4a79a-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="4a79a-137">Чтобы скопировать большую часть свойств папки, вызовите **IMAPIProp::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="4a79a-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="4a79a-138">Например, если вы хотите скопировать свойства **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и **PR_COMMENT** ([PidTagComment),](pidtagcomment-canonical-property.md)у вас есть следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="4a79a-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="4a79a-139">Вызовите **IMAPIFolder::CopyFolder,** чтобы скопировать все свойства папки, а затем удалить ненужные из новой папки.</span><span class="sxs-lookup"><span data-stu-id="4a79a-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="4a79a-140">Вызовите **CopyTo** и исключить все свойства папки, **кроме** PR_DISPLAY_NAME и **PR_COMMENT.**</span><span class="sxs-lookup"><span data-stu-id="4a79a-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="4a79a-141">Вызовите **CopyProps,** **передав PR_DISPLAY_NAME** и **PR_COMMENT** в массив include.</span><span class="sxs-lookup"><span data-stu-id="4a79a-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="4a79a-142">В этом случае **copyProps** является лучшим выбором, так как он предназначен для копирования небольшого набора свойств и является самым простым вызовом для реализации.</span><span class="sxs-lookup"><span data-stu-id="4a79a-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="4a79a-143">Чтобы скопировать или переместить только свойства папки, не включая сообщения, вызовите метод **IMAPIProp::CopyTo** папки и исключите следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="4a79a-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="4a79a-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4a79a-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="4a79a-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4a79a-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="4a79a-146">Методы копирования могут возвращать S_OK, указывая общий успех, MAPI_W_PARTIAL_COMPLETION, обозначая частичный успех или ошибку.</span><span class="sxs-lookup"><span data-stu-id="4a79a-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="4a79a-147">Если MAPI_W_PARTIAL_COMPLETION возвращается, используйте **макрос** HR_FAILED для доступа к более конкретной ошибке.</span><span class="sxs-lookup"><span data-stu-id="4a79a-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="4a79a-148">Дополнительные сведения см. в теме ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="4a79a-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="4a79a-149">Если вы копируете сообщения из одного хранилище сообщений в другое, и Юникод не поддерживается обоими, следует помнить, что данные могут быть потеряны из-за преобразования страницы кода.</span><span class="sxs-lookup"><span data-stu-id="4a79a-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="4a79a-150">Обычно вы не знаете, поддерживают ли в сообщении один или оба формата, что делает невозможным определение того, следует ли копировать текстовые свойства в виде строк ASCII или Юникод.</span><span class="sxs-lookup"><span data-stu-id="4a79a-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="4a79a-151">Если вы поддерживаете Юникод, попробуйте выполнить копирование Юникод; В случае с ошибкой со значением ошибки MAPI_E_BAD_CHARWIDTH asCII.</span><span class="sxs-lookup"><span data-stu-id="4a79a-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

