---
title: Общие элементы Outlook
TOCTitle: General Outlook items
ms:assetid: e7d57811-17b6-4689-b2fc-8eddddcbb6ba
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292516(v=office.15)
ms:contentKeyID: 55119843
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4133baf2a1b8c84ab887896e4c563fe0f8ece533
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701475"
---
# <a name="general-outlook-items"></a><span data-ttu-id="e0657-102">Общие элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="e0657-102">General Outlook items</span></span>

<span data-ttu-id="e0657-103">В этом разделе представлен пример кода, который применяется к элементам в Microsoft Outlook в общем случае.</span><span class="sxs-lookup"><span data-stu-id="e0657-103">This section provides sample code that applies to items in Microsoft Outlook in general.</span></span>

<span data-ttu-id="e0657-104">Этот раздел содержит пример кода, применимый для большинства элементов Outlook.</span><span class="sxs-lookup"><span data-stu-id="e0657-104">This section includes sample code that is applicable to most Outlook items.</span></span> <span data-ttu-id="e0657-105">Дополнительные примеры доступны в разделах, посвященных объектам [\_AppointmentItem](https://msdn.microsoft.com/library/bb623692\(v=office.15\)), [\_ContactItem](https://msdn.microsoft.com/library/bb643903\(v=office.15\)) и [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e0657-105">Further examples are available under sections specific for the [\_AppointmentItem](https://msdn.microsoft.com/library/bb623692\(v=office.15\)), [\_ContactItem](https://msdn.microsoft.com/library/bb643903\(v=office.15\)), and [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e0657-106">В этой статье</span><span class="sxs-lookup"><span data-stu-id="e0657-106">In this section</span></span>

|<span data-ttu-id="e0657-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="e0657-107">Topic</span></span>|<span data-ttu-id="e0657-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e0657-108">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="e0657-109">Создание вспомогательного класса для доступа к общим элементам Outlook</span><span class="sxs-lookup"><span data-stu-id="e0657-109">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) |<span data-ttu-id="e0657-110">Реализация вспомогательного класса OutlookItem, который обращается к общим свойствам и методам элементов Outlook, не расходуя чрезмерные ресурсы на тестирование и выполняя приведение к определенному объекту элемента перед обращением к этим элементам.</span><span class="sxs-lookup"><span data-stu-id="e0657-110">Implements an OutlookItem helper class that accesses common properties and methods of Outlook item objects, saving the overhead of testing for and casting to a specific item object before accessing these members.</span></span> <span data-ttu-id="e0657-111">Преимущества этого вспомогательного класса используются в нескольких других практических статьях, указанных в разделе "См. также".</span><span class="sxs-lookup"><span data-stu-id="e0657-111">Several other how-to topics listed in the See also section take advantage of this helper class.</span></span>|
|[<span data-ttu-id="e0657-112">Отображение выбранных элементов в активном проводнике</span><span class="sxs-lookup"><span data-stu-id="e0657-112">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)  |<span data-ttu-id="e0657-113">Удобное отображение всех выбранных элементов в активном окне проводника с помощью вспомогательного класса OutlookItem.</span><span class="sxs-lookup"><span data-stu-id="e0657-113">Uses the OutlookItem helper class to conveniently display all the items selected in the active Explorer window.</span></span>|

## <a name="see-also"></a><span data-ttu-id="e0657-114">См. также</span><span class="sxs-lookup"><span data-stu-id="e0657-114">See also</span></span>

- [<span data-ttu-id="e0657-115">Открытие и отображение содержимого файла iCalendar</span><span class="sxs-lookup"><span data-stu-id="e0657-115">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)
- [<span data-ttu-id="e0657-116">Назначение категорий элементу</span><span class="sxs-lookup"><span data-stu-id="e0657-116">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)
- [<span data-ttu-id="e0657-117">Реализация оболочки для инспекторов и отслеживание событий уровня элемента в каждом инспекторе</span><span class="sxs-lookup"><span data-stu-id="e0657-117">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)
- [<span data-ttu-id="e0657-118">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="e0657-118">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)


