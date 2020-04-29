---
title: Folders
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecf342c54d1aa2020fbfad4175a220b2aefecbe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327184"
---
# <a name="folders"></a><span data-ttu-id="7bf44-102">Папки</span><span class="sxs-lookup"><span data-stu-id="7bf44-102">Folders</span></span>

<span data-ttu-id="7bf44-p101">В этом разделе приведены примеры задач, в которых используются папки. Объекты [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) представляют иерархию папок, в которой хранятся элементы Microsoft Outlook. К таким папкам относятся папки календаря, почты и удаленных элементов. В основной сборке взаимодействия Outlook (PIA) элементы объекта **Folder** предоставляются в виде элементов объекта [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7bf44-p101">This section provides sample tasks that involve folders. [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) objects represent the folder hierarchy where Microsoft Outlook items are stored. Examples of folders include the Calendar, Mail, and Deleted Items folders. In the Outlook Primary Interop Assembly (PIA), members of the **Folder** object are exposed as members of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7bf44-107">В этой статье</span><span class="sxs-lookup"><span data-stu-id="7bf44-107">In this section</span></span>

|<span data-ttu-id="7bf44-108">Статья</span><span class="sxs-lookup"><span data-stu-id="7bf44-108">Topic</span></span>|<span data-ttu-id="7bf44-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7bf44-109">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="7bf44-110">Добавление папки в список папок</span><span class="sxs-lookup"><span data-stu-id="7bf44-110">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md) |<span data-ttu-id="7bf44-111">Использование метода [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) для добавления папки в список папок Outlook.</span><span class="sxs-lookup"><span data-stu-id="7bf44-111">Uses the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add a folder to the Outlook folder list.</span></span>|
|[<span data-ttu-id="7bf44-112">Перечисление папок</span><span class="sxs-lookup"><span data-stu-id="7bf44-112">Enumerate folders</span></span>](how-to-enumerate-folders.md)  |<span data-ttu-id="7bf44-113">Перечисление папок путем итерации по коллекциям папок.</span><span class="sxs-lookup"><span data-stu-id="7bf44-113">Enumerates folders by iterating through a collection of folders.</span></span>|
|[<span data-ttu-id="7bf44-114">Получение папки по умолчанию и перечисление вложенных в нее папок</span><span class="sxs-lookup"><span data-stu-id="7bf44-114">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |<span data-ttu-id="7bf44-115">Получение папки по умолчанию в хранилище по умолчанию пользователя и перечисление вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="7bf44-115">Obtains a default folder in the user’s default store and enumerates its subfolders.</span></span>|
|[<span data-ttu-id="7bf44-116">Получение папки на основе пути к ней</span><span class="sxs-lookup"><span data-stu-id="7bf44-116">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)  |<span data-ttu-id="7bf44-117">Использование пути к папке и получение связанной папки.</span><span class="sxs-lookup"><span data-stu-id="7bf44-117">Takes a folder path and obtains the associated folder.</span></span>|
|[<span data-ttu-id="7bf44-118">Выбор папки и отображение сведений о папке</span><span class="sxs-lookup"><span data-stu-id="7bf44-118">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)  |<span data-ttu-id="7bf44-119">Отображение программным способом сведений о папке, выбранной пользователем из определенного списка папок.</span><span class="sxs-lookup"><span data-stu-id="7bf44-119">Programmatically displays information about a folder that a user selects from a specified folder list.</span></span>|
|[<span data-ttu-id="7bf44-120">Получение класса сообщений по умолчанию для папки</span><span class="sxs-lookup"><span data-stu-id="7bf44-120">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)  |<span data-ttu-id="7bf44-121">Использование свойства [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) для получения класса сообщений по умолчанию для папки.</span><span class="sxs-lookup"><span data-stu-id="7bf44-121">Uses the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>|
|[<span data-ttu-id="7bf44-122">Доступ к данным решений, хранящимся в скрытом сообщении в папке</span><span class="sxs-lookup"><span data-stu-id="7bf44-122">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |<span data-ttu-id="7bf44-123">Использование объекта [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) для извлечения данных, которые хранятся в виде скрытого сообщения определенного класса сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="7bf44-123">Uses the [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) object to retrieve data that is stored as a hidden message of a specific message class in a folder.</span></span>|
|[<span data-ttu-id="7bf44-124">Проверка поддержки настраиваемых свойств элемента в запросах на уровне папки</span><span class="sxs-lookup"><span data-stu-id="7bf44-124">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |<span data-ttu-id="7bf44-125">Проверка того, что при добавлении настраиваемого свойства к типу элемента в папку также добавляется свойство, обеспечивающее запрос настраиваемого свойства на уровне папки.</span><span class="sxs-lookup"><span data-stu-id="7bf44-125">Shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>|

## <a name="see-also"></a><span data-ttu-id="7bf44-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7bf44-126">See also</span></span>

- [<span data-ttu-id="7bf44-127">Календарь</span><span class="sxs-lookup"><span data-stu-id="7bf44-127">Calendar</span></span>](calendar.md)
- [<span data-ttu-id="7bf44-128">Контакты</span><span class="sxs-lookup"><span data-stu-id="7bf44-128">Contacts</span></span>](contacts.md)
- [<span data-ttu-id="7bf44-129">Почта</span><span class="sxs-lookup"><span data-stu-id="7bf44-129">Mail</span></span>](mail.md)
- [<span data-ttu-id="7bf44-130">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="7bf44-130">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

