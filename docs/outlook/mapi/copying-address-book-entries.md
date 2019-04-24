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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333070"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="6307b-103">Копирование записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="6307b-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="6307b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6307b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6307b-105">Ваш контейнер [иабконтаинер:: копентриес](iabcontainer-copyentries.md) вызывается при копировании одного или нескольких получателей из одного или другого контейнера в этот контейнер.</span><span class="sxs-lookup"><span data-stu-id="6307b-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="6307b-106">**Копентриес** имеет четыре входных параметра: массив идентификаторов записей, представляющих копируемых получателей, дескриптор окна для индикатора хода выполнения, указатель на объект хода выполнения и значение флагов.</span><span class="sxs-lookup"><span data-stu-id="6307b-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="6307b-107">Поставщик должен отображать ход выполнения, если флаг АБ_НО_ДИАЛОГ не задан, и использовать объект Progress из параметра _лппрогресс_ , если он не имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="6307b-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="6307b-108">Если _лппрогресс_ имеет значение null, вызовите [Имаписуппорт::D опрогрессдиалог](imapisupport-doprogressdialog.md) , чтобы использовать объект Progress MAPI.</span><span class="sxs-lookup"><span data-stu-id="6307b-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="6307b-109">Для получения дополнительных сведений об отображении [индикатора хода выполнения](mapi-progress-indicators.md)см.</span><span class="sxs-lookup"><span data-stu-id="6307b-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="6307b-110">В дополнение к АБ_НО_ДИАЛОГ, чтобы отключить индикатор хода выполнения, можно задать один из двух других флагов, чтобы запросить тип проверки повторяющихся записей: КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ или КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ.</span><span class="sxs-lookup"><span data-stu-id="6307b-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="6307b-111">Флаги КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ и КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ представляют собой только варианты, определяющие, как поставщик определяет дублирующиеся записи и может быть проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="6307b-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="6307b-112">MAPI предлагает поставщику поддержку этих флагов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="6307b-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="6307b-113">**Повторяющийся флаг записи**</span><span class="sxs-lookup"><span data-stu-id="6307b-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="6307b-114">**Предлагаемая реализация**</span><span class="sxs-lookup"><span data-stu-id="6307b-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6307b-115">КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ</span><span class="sxs-lookup"><span data-stu-id="6307b-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="6307b-116">Убедитесь, что отображаемое имя в создаваемой записи совпадает с отображаемым именем записи, которая уже находится в контейнере.</span><span class="sxs-lookup"><span data-stu-id="6307b-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="6307b-117">КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ</span><span class="sxs-lookup"><span data-stu-id="6307b-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="6307b-118">Убедитесь, что отображаемое имя и ключ поиска в записи совпадают с отображаемым именем и ключом поиска записи контейнера.</span><span class="sxs-lookup"><span data-stu-id="6307b-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="6307b-119">Последний флаг, КРЕАТЕ_РЕПЛАЦЕ, указывает, что новая запись должна заменить существующую, если у поставщика определено, что создаваемая запись является дубликатом записи, которая уже находится в контейнере.</span><span class="sxs-lookup"><span data-stu-id="6307b-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="6307b-120">Если ваш поставщик является личной адресной книгой, включите свойство **пр_детаилс_табле** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) в каждую операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="6307b-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="6307b-121">Включение таблицы отображения сведений для скопированного получателя позволяет контейнеру отображать сведения о получателе, а не вызывать исходный контейнер для создания отображения.</span><span class="sxs-lookup"><span data-stu-id="6307b-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="6307b-122">**Реализация Иабконтаинер:: Копентриес**</span><span class="sxs-lookup"><span data-stu-id="6307b-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="6307b-123">Определите, является ли каждый идентификатор записи в параметре _лпентриес_ форматом, который обрабатывается поставщиком, а также в случае, если это не так, отработка отказа и возврат мапи_е_инвалид_ентрид.</span><span class="sxs-lookup"><span data-stu-id="6307b-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="6307b-124">Если идентификатор записи представляет пользователя обмена сообщениями, список рассылки или контейнер, который обрабатывает ваш поставщик:</span><span class="sxs-lookup"><span data-stu-id="6307b-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="6307b-125">ВыЗовите метод [имаписуппорт:: OpenEntry](imapisupport-openentry.md) , чтобы открыть соответствующий получатель.</span><span class="sxs-lookup"><span data-stu-id="6307b-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="6307b-126">Скопируйте получателя в свой контейнер.</span><span class="sxs-lookup"><span data-stu-id="6307b-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="6307b-127">Если идентификатор записи представляет инородного получателя:</span><span class="sxs-lookup"><span data-stu-id="6307b-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="6307b-128">ВыЗовите свой контейнер [иабконтаинер:: креатинтри](iabcontainer-createentry.md) , чтобы создать нового получателя.</span><span class="sxs-lookup"><span data-stu-id="6307b-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="6307b-129">Задайте исходные свойства для нового получателя.</span><span class="sxs-lookup"><span data-stu-id="6307b-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="6307b-130">ВыЗовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) нового объекта, чтобы сохранить его.</span><span class="sxs-lookup"><span data-stu-id="6307b-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="6307b-131">Обновите таблицу содержимого контейнера в соответствии с новым получателем.</span><span class="sxs-lookup"><span data-stu-id="6307b-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="6307b-132">Call [имаписуппорт:: notify](imapisupport-notify.md) для отправки табличного уведомления зарегистрированным клиентам.</span><span class="sxs-lookup"><span data-stu-id="6307b-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

