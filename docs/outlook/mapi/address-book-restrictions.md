---
title: Ограничения адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432802"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="5c04e-103">Ограничения адресной книги</span><span class="sxs-lookup"><span data-stu-id="5c04e-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="5c04e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c04e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c04e-105">Поставщики адресных книг должны поддерживать три типа ограничений для таблиц содержимого контейнеров:</span><span class="sxs-lookup"><span data-stu-id="5c04e-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="5c04e-106">Неоднозначные ограничения свойств имени</span><span class="sxs-lookup"><span data-stu-id="5c04e-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="5c04e-107">Например, ограничения ключевых свойств</span><span class="sxs-lookup"><span data-stu-id="5c04e-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="5c04e-108">Ограничения контента с префиксом отображаемой фамилии</span><span class="sxs-lookup"><span data-stu-id="5c04e-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="5c04e-109">Неоднозначные ограничения имен — это ограничения свойств с помощью **свойства PR_ANR** [(PidTagAnr)](pidtaganr-canonical-property.md)для совпадения имен получателей с записями в контейнерах адресной книги.</span><span class="sxs-lookup"><span data-stu-id="5c04e-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="5c04e-110">Ограничение **PR_ANR** — это тип поиска с наилучшими предположениями, в котором поставщики адресных книг могут выбрать свойство, которое лучше всего работает для контейнера.</span><span class="sxs-lookup"><span data-stu-id="5c04e-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="5c04e-111">Например, один поставщик адресных книг может реализовать ограничение **PR_ANR** путем совпадения имен получателей с свойством **PR_ACCOUNT** [(PidTagAccount)](pidtagaccount-canonical-property.md)каждой записи контейнера, в то время как другой поставщик может использовать **PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c04e-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="5c04e-112">MAPI рекомендует, чтобы реализация ограничения PR_ANR **баланс** между адекватной производительностью и удовлетворенность пользователей.</span><span class="sxs-lookup"><span data-stu-id="5c04e-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="5c04e-113">Удовлетворенность пользователей может быть скомпрометирована, когда поставщик адресной книги реализует ограничение таким образом, что обнаружено слишком мало совпадений или слишком много совпадений.</span><span class="sxs-lookup"><span data-stu-id="5c04e-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="5c04e-114">Некоторые поставщики адресных книг поддерживают имя, которое не отображается в диалоговом окне, но может соответствовать двусмысленным ограничениям имен.</span><span class="sxs-lookup"><span data-stu-id="5c04e-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="5c04e-115">Типичной реализацией может быть размыть имя отображения получателя на слова, сообразуя все записи, которые содержат все слова.</span><span class="sxs-lookup"><span data-stu-id="5c04e-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="5c04e-116">Внимание к таким деталям, как чувствительность к позиции слова, соответствие неконсектативных слов и выбор символов сепаратора может отличаться.</span><span class="sxs-lookup"><span data-stu-id="5c04e-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="5c04e-117">Например, если разрешено имя "Bill **L",** типичное ограничение PR_ANR для выбора следующих записей в качестве совпадения:</span><span class="sxs-lookup"><span data-stu-id="5c04e-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="5c04e-118">Билли Ларсон</span><span class="sxs-lookup"><span data-stu-id="5c04e-118">Billy Larson</span></span>
    
- <span data-ttu-id="5c04e-119">Билл Ли</span><span class="sxs-lookup"><span data-stu-id="5c04e-119">Bill Lee</span></span>
    
- <span data-ttu-id="5c04e-120">Билл Логан-младший</span><span class="sxs-lookup"><span data-stu-id="5c04e-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="5c04e-121">Ли, Сэм Билл</span><span class="sxs-lookup"><span data-stu-id="5c04e-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="5c04e-122">В реализации полей списков, используемых в клиентских **приложениях** для просмотра таблиц MAPI, используются основные ограничения экземпляра или ограничения PR_INSTANCE_KEY [(PidTagInstanceKey).](pidtaginstancekey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c04e-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="5c04e-123">Некоторые реализации поле списка позволяют пользователям делать несколько выборов, прокручивать вверх или вниз и возвращаться к выбранному первому элементу.</span><span class="sxs-lookup"><span data-stu-id="5c04e-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="5c04e-124">Для реализации этого поведения клиенты называют [IMAPITable::FindRow,](imapitable-findrow.md) **передавая** методу ограничение свойств PR_INSTANCE_KEY свойства.</span><span class="sxs-lookup"><span data-stu-id="5c04e-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="5c04e-125">Поставщики адресных книг должны поддерживать это ограничение.</span><span class="sxs-lookup"><span data-stu-id="5c04e-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="5c04e-126">Еще одна особенность полей списков, используемых для просмотра таблицы, — это возможность расположить курсор на основе набора символов префикса.</span><span class="sxs-lookup"><span data-stu-id="5c04e-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="5c04e-127">Когда пользователь начинает вводить символы префикса, клиент перемещает курсор на первый элемент, который начинается с этих символов.</span><span class="sxs-lookup"><span data-stu-id="5c04e-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="5c04e-128">Клиенты реализуют эту функцию с ограничением контента на основе свойства PR_DISPLAY_NAME **и** FL_PREFIX нечеткого уровня.</span><span class="sxs-lookup"><span data-stu-id="5c04e-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c04e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5c04e-129">See also</span></span>



[<span data-ttu-id="5c04e-130">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="5c04e-130">MAPI Tables</span></span>](mapi-tables.md)

