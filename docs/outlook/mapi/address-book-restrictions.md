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
ms.openlocfilehash: 54cd90cac6c00e8cf274e0b78a1bfec32401bb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576514"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="69853-103">Ограничения для адресных книг</span><span class="sxs-lookup"><span data-stu-id="69853-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="69853-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69853-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69853-105">Поставщиками адресной книги необходимо поддерживает три типа ограничений на содержимое таблицы их контейнеров:</span><span class="sxs-lookup"><span data-stu-id="69853-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="69853-106">Ограничения свойств неоднозначное имя</span><span class="sxs-lookup"><span data-stu-id="69853-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="69853-107">Ограничения ключевых свойств экземпляра</span><span class="sxs-lookup"><span data-stu-id="69853-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="69853-108">Ограничения на имена с префиксами отображения содержимого</span><span class="sxs-lookup"><span data-stu-id="69853-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="69853-109">Ограничения разрешения неоднозначных псевдонимов, ограничений свойств с помощью свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) в соответствии с получателей с записями контейнеры адресной книги.</span><span class="sxs-lookup"><span data-stu-id="69853-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="69853-110">Ограничение свойства **PR_ANR** — это тип «лучше всего подбора» поиска, при котором поставщиками адресных книг можно выбрать соответствующее свойство, которое лучше всего подходит для их контейнера.</span><span class="sxs-lookup"><span data-stu-id="69853-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="69853-111">Например один поставщик адресной книги может внедрить ограничение **PR_ANR** с совпадающим имена получателей свойство **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) для каждой записи контейнер то время как другой поставщик может использовать **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="69853-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="69853-112">MAPI рекомендует, что реализации ограничения **PR_ANR** соблюсти баланс между достаточной производительности и уровня удовлетворенности пользователей.</span><span class="sxs-lookup"><span data-stu-id="69853-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="69853-113">Удовлетворенность пользователей могут быть раскрыты при поставщика адресных книг реализует ограничение таким образом, что слишком мало или слишком много совпадений.</span><span class="sxs-lookup"><span data-stu-id="69853-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="69853-114">Некоторые поставщиками адресных книг поддерживает как различающееся или общие, имя, которое не отображаемых в диалоговом окне, но можно сопоставить неоднозначное имя ограничения.</span><span class="sxs-lookup"><span data-stu-id="69853-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="69853-115">Типичное использование возможно для анализа получателя отображаемое имя на слова, сопоставляя любой элемент, который содержит все из ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="69853-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="69853-116">Внимание на сведения, например знаков в word позицию, сопоставляются ли слова, расположенные в разных местах и выбор разделители могут различаться.</span><span class="sxs-lookup"><span data-stu-id="69853-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="69853-117">Например если разрешаться называется «Bill L», типичные ограничения **PR_ANR** выделить следующие записи как совпадение:</span><span class="sxs-lookup"><span data-stu-id="69853-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="69853-118">Билли Larson</span><span class="sxs-lookup"><span data-stu-id="69853-118">Billy Larson</span></span>
    
- <span data-ttu-id="69853-119">Билл Иванов</span><span class="sxs-lookup"><span data-stu-id="69853-119">Bill Lee</span></span>
    
- <span data-ttu-id="69853-120">Билл заявок игре на персонал.</span><span class="sxs-lookup"><span data-stu-id="69853-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="69853-121">Сэм Билл Иванов</span><span class="sxs-lookup"><span data-stu-id="69853-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="69853-122">Экземпляр ключевых ограничений или ограничений свойств **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), используются в реализации списков, которые используются в клиентских приложениях для просмотра таблиц MAPI.</span><span class="sxs-lookup"><span data-stu-id="69853-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="69853-123">Некоторые реализации поле списка пользователи могут выбрать несколько элементов, прокрутить вверх или вниз и возврата к первому элементу.</span><span class="sxs-lookup"><span data-stu-id="69853-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="69853-124">Чтобы реализовать это поведение, клиенты вызывать [IMAPITable::FindRow](imapitable-findrow.md), передав ограничение свойства на свойство **PR_INSTANCE_KEY** методу.</span><span class="sxs-lookup"><span data-stu-id="69853-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="69853-125">Для поддержки это ограничение требуются поставщиками адресной книги.</span><span class="sxs-lookup"><span data-stu-id="69853-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="69853-126">Другого компонента из списка полей, используется для просмотра в таблице является возможность наведите указатель на основе набора символов префикса.</span><span class="sxs-lookup"><span data-stu-id="69853-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="69853-127">Как пользователь начинает ввод символы префикса, клиент перемещает курсор в первый элемент, который начинается с этих символов.</span><span class="sxs-lookup"><span data-stu-id="69853-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="69853-128">Клиенты с ограничением контента на основе свойства **PR_DISPLAY_NAME** и уровень Нечеткое FL_PREFIX реализация этой возможности.</span><span class="sxs-lookup"><span data-stu-id="69853-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69853-129">См. также</span><span class="sxs-lookup"><span data-stu-id="69853-129">See also</span></span>



[<span data-ttu-id="69853-130">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="69853-130">MAPI Tables</span></span>](mapi-tables.md)

