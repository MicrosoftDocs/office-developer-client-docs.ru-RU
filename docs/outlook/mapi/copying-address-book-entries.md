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
ms.openlocfilehash: ce7f7e2db341be62912935b7a55d69eaf5db8ab5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808205"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="de434-103">Копирование записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="de434-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="de434-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de434-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de434-105">При вызове метода [IABContainer::CopyEntries](iabcontainer-copyentries.md) контейнера одного или нескольких получателей из того же или другой контейнер, должны быть скопированы в этот контейнер.</span><span class="sxs-lookup"><span data-stu-id="de434-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="de434-106">**CopyEntries** имеет четыре входных параметров: массив идентификаторов записи, представляющее получателей для копирования, дескриптор окна для индикатора, указатель объекта хода выполнения и значение флагов.</span><span class="sxs-lookup"><span data-stu-id="de434-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="de434-107">Поставщик должен отображаться ход выполнения, если не задан флаг AB_NO_DIALOG и используйте объект о ходе выполнения с помощью параметра _lpProgress_ , если он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="de434-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="de434-108">Если _lpProgress_ имеет значение NULL, вызовите [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) использовать объект MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="de434-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="de434-109">Дополнительные сведения об отображении хода выполнения [отображая индикатор выполнения](mapi-progress-indicators.md)см.</span><span class="sxs-lookup"><span data-stu-id="de434-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="de434-110">В дополнение к AB_NO_DIALOG для отмены вывода индикатор хода выполнения один из двух флагов можно задать тип проверки дубликат запроса: CREATE_CHECK_DUP_LOOSE или CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="de434-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="de434-111">Флаги CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT только предложения, как, чтобы как поставщика определяет повторяющихся записей и можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="de434-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="de434-112">MAPI предполагает, что ваш поставщик реализации поддержки эти флаги следующим образом.</span><span class="sxs-lookup"><span data-stu-id="de434-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="de434-113">**Флаг Повторяющаяся запись**</span><span class="sxs-lookup"><span data-stu-id="de434-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="de434-114">**Предлагаемые реализации**</span><span class="sxs-lookup"><span data-stu-id="de434-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de434-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="de434-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="de434-116">Проверьте, если отображаемое имя в записи, которую требуется создать соответствует отображаемое имя записи уже в контейнере.</span><span class="sxs-lookup"><span data-stu-id="de434-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="de434-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="de434-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="de434-118">Убедитесь, если отображаемое имя и ключа поиска в записи, которую требуется создать соответствуют отображаемое имя и поиска ключ записи контейнера.</span><span class="sxs-lookup"><span data-stu-id="de434-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="de434-119">Последний флаг CREATE_REPLACE, указывает, что новая запись необходимо заменить существующий, если ваш поставщик обнаружила, что запись будет создан дубликат запись уже в контейнере.</span><span class="sxs-lookup"><span data-stu-id="de434-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="de434-120">Если ваш поставщик Личная адресная книга, включите свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) для каждой операции копирования.</span><span class="sxs-lookup"><span data-stu-id="de434-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="de434-121">Включая в таблице отображения сведений о скопированной получателя позволяет контейнера для отображения сведений о получателя, а не прибегая к исходной контейнер для создания отображения.</span><span class="sxs-lookup"><span data-stu-id="de434-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="de434-122">**Для реализации IABContainer::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="de434-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="de434-123">Определение возможности каждого идентификатор записи с помощью параметра _lpEntries_ в виде, ваш поставщик обрабатывает и если это не так, с ошибкой и возвращать MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="de434-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="de434-124">Если обмена сообщениями пользователя, список рассылки или контейнера, обрабатывающего ваш поставщик представляет идентификатор записи:</span><span class="sxs-lookup"><span data-stu-id="de434-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="de434-125">Вызовите метод [IMAPISupport::OpenEntry](imapisupport-openentry.md) для открытия соответствующего получателя.</span><span class="sxs-lookup"><span data-stu-id="de434-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="de434-126">Скопируйте получателя контейнера.</span><span class="sxs-lookup"><span data-stu-id="de434-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="de434-127">Если идентификатор записи представляет внешнего получателя:</span><span class="sxs-lookup"><span data-stu-id="de434-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="de434-128">Вызов метода [IABContainer::CreateEntry](iabcontainer-createentry.md) контейнера для создания нового получателя.</span><span class="sxs-lookup"><span data-stu-id="de434-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="de434-129">Задавать начальные свойства нового получателя.</span><span class="sxs-lookup"><span data-stu-id="de434-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="de434-130">Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новый объект для его сохранения.</span><span class="sxs-lookup"><span data-stu-id="de434-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="de434-131">Обновление таблицы содержимого контейнера в соответствии с новой получателя.</span><span class="sxs-lookup"><span data-stu-id="de434-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="de434-132">Вызов [IMAPISupport::Notify](imapisupport-notify.md) для отправки уведомлений в таблице зарегистрированным пользователям.</span><span class="sxs-lookup"><span data-stu-id="de434-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

