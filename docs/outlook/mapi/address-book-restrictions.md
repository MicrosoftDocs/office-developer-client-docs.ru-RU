---
title: Ограничения для адресных книг
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328079"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="4fffb-103">Ограничения для адресных книг</span><span class="sxs-lookup"><span data-stu-id="4fffb-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="4fffb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fffb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fffb-105">Поставщики адресных книг необходимы для поддержки трех типов ограничений в таблицах контента их контейнеров:</span><span class="sxs-lookup"><span data-stu-id="4fffb-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="4fffb-106">Ограничения свойств неОднозначного имени</span><span class="sxs-lookup"><span data-stu-id="4fffb-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="4fffb-107">Ограничения свойств ключа экземпляра</span><span class="sxs-lookup"><span data-stu-id="4fffb-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="4fffb-108">Ограничения на содержимое предопределенного отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="4fffb-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="4fffb-109">Ограничения неоднозначных имен — это ограничения свойств с помощью свойства **пр_анр** ([PidTagAnr](pidtaganr-canonical-property.md)) для согласования имен получателей с записями в контейнерах адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4fffb-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="4fffb-110">Ограничение свойства **пр_анр** — это "оптимальный тип поиска", при котором поставщики адресных книг могут выбрать соответствующее свойство, которое лучше всего подходит для контейнера.</span><span class="sxs-lookup"><span data-stu-id="4fffb-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="4fffb-111">Например, один поставщик адресных книг может реализовать ограничение **пр_анр** , сопоставляя имена получателей с свойством **пр_аккаунт** ([PidTagAccount](pidtagaccount-canonical-property.md)) каждой записи контейнера, в то время как другой поставщик может использовать **пр_дисплай _НАМЕ** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4fffb-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="4fffb-112">MAPI рекомендует применение ограничения **пр_анр** для обеспечения баланса между адекватной производительностью и степенью удовлетворенности пользователей.</span><span class="sxs-lookup"><span data-stu-id="4fffb-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="4fffb-113">Степень удовлетворенности пользователей может быть нарушена, когда поставщик адресных книг реализует ограничение таким образом, что найдено слишком мало или слишком много совпадений.</span><span class="sxs-lookup"><span data-stu-id="4fffb-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="4fffb-114">Некоторые поставщики адресных книг поддерживают то, что называется различающимся или распространенным именем, которое не поддерживается в диалоговом окне, но может сопоставляться с ограничением неоднозначных имен.</span><span class="sxs-lookup"><span data-stu-id="4fffb-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="4fffb-115">Типичной реализацией может быть анализ отображаемого имени получателя в словах, что соответствует любой записи, содержащей все слова.</span><span class="sxs-lookup"><span data-stu-id="4fffb-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="4fffb-116">Обратите внимание на такие сведения, как положение в слове, независимо от того, совпадают ли непоследовательные слова, а также может ли выбираться разделитель символов.</span><span class="sxs-lookup"><span data-stu-id="4fffb-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="4fffb-117">Например, если имя, которое необходимо разрешить, — "Билл L", то типичное ограничение **пр_анр** будет выбирать следующие записи в качестве совпадений:</span><span class="sxs-lookup"><span data-stu-id="4fffb-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="4fffb-118">Билли Ларсон</span><span class="sxs-lookup"><span data-stu-id="4fffb-118">Billy Larson</span></span>
    
- <span data-ttu-id="4fffb-119">Вексельный вексель</span><span class="sxs-lookup"><span data-stu-id="4fffb-119">Bill Lee</span></span>
    
- <span data-ttu-id="4fffb-120">Билл Логан мл.</span><span class="sxs-lookup"><span data-stu-id="4fffb-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="4fffb-121">SAM вексель Иванов</span><span class="sxs-lookup"><span data-stu-id="4fffb-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="4fffb-122">Ограничения для ключа экземпляра или ограничения свойств **пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) используются в реализации списков, которые используются в клиентских приложениях для просмотра таблиц MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fffb-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="4fffb-123">Некоторые реализации списков позволяют пользователям выбирать несколько вариантов, прокручивать их вверх или вниз и возвращаться к первому выбранному элементу.</span><span class="sxs-lookup"><span data-stu-id="4fffb-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="4fffb-124">Чтобы реализовать такое поведение, клиенты вызывают вызов [IMAPITable:: FindRow](imapitable-findrow.md), передавая ограничение свойства для свойства **пр_инстанце_кэй** в метод.</span><span class="sxs-lookup"><span data-stu-id="4fffb-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="4fffb-125">Для поддержки этого ограничения необходимы поставщики адресных книг.</span><span class="sxs-lookup"><span data-stu-id="4fffb-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="4fffb-126">Другим компонентом списков, используемым для просмотра таблиц, является возможность позиционирования курсора на основе набора символов префикса.</span><span class="sxs-lookup"><span data-stu-id="4fffb-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="4fffb-127">Когда пользователь начинает вводить префиксы, клиент перемещает курсор на первый элемент, начинающийся с этих символов.</span><span class="sxs-lookup"><span data-stu-id="4fffb-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="4fffb-128">Клиенты реализуют эту функцию с ограничением содержимого на основе свойства **пр_дисплай_наме** и нечеткого уровня фл_префикс.</span><span class="sxs-lookup"><span data-stu-id="4fffb-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4fffb-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4fffb-129">See also</span></span>



[<span data-ttu-id="4fffb-130">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="4fffb-130">MAPI Tables</span></span>](mapi-tables.md)

