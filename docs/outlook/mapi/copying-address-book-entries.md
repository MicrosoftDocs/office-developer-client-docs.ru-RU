---
title: Копирование записей адресной книги
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418745"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="a91c5-103">Копирование записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="a91c5-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="a91c5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a91c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a91c5-105">Метод [IABContainer::CopyEntries](iabcontainer-copyentries.md) вашего контейнера вызван, когда один или несколько получателей из одного или других контейнеров копируется в этот контейнер.</span><span class="sxs-lookup"><span data-stu-id="a91c5-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="a91c5-106">**CopyEntries** имеет четыре входных параметра: массив идентификаторов записей, представляющих получателей, которые необходимо скопировать, окне для индикатора хода выполнения, указатель объекта хода выполнения и значение флагов.</span><span class="sxs-lookup"><span data-stu-id="a91c5-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="a91c5-107">Поставщик должен отобразить ход выполнения, если флаг AB_NO_DIALOG не установлен, и использовать объект хода выполнения из параметра  _lpProgress,_ если он не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="a91c5-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="a91c5-108">Если  _lpProgress_ имеет NULL, вызовите [IMAPISupport::D oProgressDialog,](imapisupport-doprogressdialog.md) чтобы использовать объект хода выполнения MAPI.</span><span class="sxs-lookup"><span data-stu-id="a91c5-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="a91c5-109">Дополнительные сведения о ходе выполнения см. в этой [теме.](mapi-progress-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="a91c5-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="a91c5-110">Помимо AB_NO_DIALOG для подавления индикатора хода выполнения, можно настроить один из двух других флагов для запроса типа проверки дубликатов записей: CREATE_CHECK_DUP_LOOSE или CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="a91c5-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="a91c5-111">Флаги CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT являются лишь рекомендациями о том, как поставщик определяет повторяющиеся записи и может игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a91c5-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="a91c5-112">MAPI предлагает поставщику реализовать поддержку этих флагов следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a91c5-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="a91c5-113">**Дубликат флага записи**</span><span class="sxs-lookup"><span data-stu-id="a91c5-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="a91c5-114">**Рекомендуемая реализация**</span><span class="sxs-lookup"><span data-stu-id="a91c5-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a91c5-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="a91c5-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="a91c5-116">Проверьте, соответствует ли отображаемого имени создаемой записи отображаемого имени уже в контейнере.</span><span class="sxs-lookup"><span data-stu-id="a91c5-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="a91c5-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="a91c5-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="a91c5-118">Проверьте, совпадают ли отображаемая и поисковая клавиша в создаемой записи с отображаемой и поисковой клавишами записи контейнера.</span><span class="sxs-lookup"><span data-stu-id="a91c5-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="a91c5-119">Последний флаг, CREATE_REPLACE, указывает, что новая запись должна заменить существующую, если поставщик определил, что создаемая запись является дубликатом записи, уже имеющейся в контейнере.</span><span class="sxs-lookup"><span data-stu-id="a91c5-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="a91c5-120">Если ваш поставщик является личной адресной книгой, **включите свойство PR_DETAILS_TABLE** ([PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)в каждую операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="a91c5-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="a91c5-121">Включив таблицу отображения сведений скопированного получателя, контейнер позволяет отображать сведения о получателе, а не вызывать исходный контейнер для создания дисплея.</span><span class="sxs-lookup"><span data-stu-id="a91c5-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="a91c5-122">**Реализация IABContainer::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="a91c5-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="a91c5-123">Определите, находится ли каждый идентификатор записи в параметре  _lpEntries_ в формате, который обрабатывает ваш поставщик, и если это не так, сбой и возврат MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="a91c5-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="a91c5-124">Если идентификатор записи представляет пользователя обмена сообщениями, список рассылки или контейнер, который обрабатывает ваш поставщик:</span><span class="sxs-lookup"><span data-stu-id="a91c5-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="a91c5-125">Вызовите метод [IMAPISupport::OpenEntry,](imapisupport-openentry.md) чтобы открыть соответствующего получателя.</span><span class="sxs-lookup"><span data-stu-id="a91c5-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="a91c5-126">Скопируйте получателя в контейнер.</span><span class="sxs-lookup"><span data-stu-id="a91c5-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="a91c5-127">Если идентификатор записи представляет внешнего получателя:</span><span class="sxs-lookup"><span data-stu-id="a91c5-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="a91c5-128">Вызовите метод [IABContainer::CreateEntry](iabcontainer-createentry.md) контейнера, чтобы создать нового получателя.</span><span class="sxs-lookup"><span data-stu-id="a91c5-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="a91c5-129">Установите начальные свойства для нового получателя.</span><span class="sxs-lookup"><span data-stu-id="a91c5-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="a91c5-130">Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) нового объекта, чтобы сохранить его.</span><span class="sxs-lookup"><span data-stu-id="a91c5-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="a91c5-131">Обновим таблицу содержимого контейнера, чтобы отразить нового получателя.</span><span class="sxs-lookup"><span data-stu-id="a91c5-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="a91c5-132">Вызов [IMAPISupport::Notify](imapisupport-notify.md) для отправки уведомлений о таблице зарегистрированным клиентам.</span><span class="sxs-lookup"><span data-stu-id="a91c5-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

