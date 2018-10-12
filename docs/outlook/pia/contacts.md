---
title: Контакты
TOCTitle: Contacts
ms:assetid: e988de54-6b1e-4e83-a226-3a898903608f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184649(v=office.15)
ms:contentKeyID: 55119820
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: a172f0ab978f2281b509ed7e848168d8daa3a0fc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406213"
---
# <a name="contacts"></a><span data-ttu-id="f6aba-102">Контакты</span><span class="sxs-lookup"><span data-stu-id="f6aba-102">Contacts</span></span>

<span data-ttu-id="f6aba-103">В этой статье приведены примеры разделов, связанные с контактами.</span><span class="sxs-lookup"><span data-stu-id="f6aba-103">This section provides sample tasks that involve appointments.</span></span> <span data-ttu-id="f6aba-104">Контакты представляют людей и организации, с которыми вы хотите взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="f6aba-104">Contacts represent people and businesses you want to communicate with.</span></span> <span data-ttu-id="f6aba-105">Папка "Контакты" — это адресная книга электронной почты и хранилище сведений о контактах.</span><span class="sxs-lookup"><span data-stu-id="f6aba-105">The Contacts folder is your email address book and information storage for the contacts.</span></span> <span data-ttu-id="f6aba-106">Объект [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) является встроенным объектом Outlook, представляющим уникальные контакты в папке "Контакты".</span><span class="sxs-lookup"><span data-stu-id="f6aba-106">A [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object is an Outlook built-in object that represents unique contacts in a Contacts folder.</span></span> <span data-ttu-id="f6aba-107">Объект **ContactItem** имеет более 100 свойств, таких как [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) и [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)), а также настраиваемые свойства, если встроенных свойств недостаточно. Настраиваемые свойства можно использовать для хранения сведений о каждом контакте.</span><span class="sxs-lookup"><span data-stu-id="f6aba-107">The **ContactItem** object has over 100 properties, such as [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), and [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)), as well as custom properties if the built-in properties are not sufficient, that you can use to store information about each contact.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f6aba-108">В этой статье</span><span class="sxs-lookup"><span data-stu-id="f6aba-108">In this section</span></span>

|<span data-ttu-id="f6aba-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="f6aba-109">Topic</span></span>|<span data-ttu-id="f6aba-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f6aba-110">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="f6aba-111">Создание элемента контакта</span><span class="sxs-lookup"><span data-stu-id="f6aba-111">Create a Contact item</span></span>](how-to-create-a-contact-item.md)  |<span data-ttu-id="f6aba-112">Создание элемента контакта и настройка различных свойств контакта.</span><span class="sxs-lookup"><span data-stu-id="f6aba-112">Creates a contact item and sets various properties for the contact.</span></span>|
|[<span data-ttu-id="f6aba-113">Создание настраиваемого элемента контакта</span><span class="sxs-lookup"><span data-stu-id="f6aba-113">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)  |<span data-ttu-id="f6aba-114">Создание настраиваемого элемента контакта и настройка предопределенных и пользовательских свойств.</span><span class="sxs-lookup"><span data-stu-id="f6aba-114">Creates a custom contact item and sets both predefined and user-defined properties.</span></span>|
|[<span data-ttu-id="f6aba-115">Создание элемента контакта из файла vCard и сохранение элемента в папку</span><span class="sxs-lookup"><span data-stu-id="f6aba-115">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)  |<span data-ttu-id="f6aba-116">Импорт всех файлов vCard в папку файловой системы и сохранение контактов в папке, заданной параметром *targetFolder*.</span><span class="sxs-lookup"><span data-stu-id="f6aba-116">Imports all the vCard files in a file system folder and saves the contacts into the folder specified by the *targetFolder* parameter.</span></span>|

## <a name="see-also"></a><span data-ttu-id="f6aba-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f6aba-117">See also</span></span>

- [<span data-ttu-id="f6aba-118">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="f6aba-118">Address Book</span></span>](address-book.md)
- [<span data-ttu-id="f6aba-119">Электронные визитные карточки</span><span class="sxs-lookup"><span data-stu-id="f6aba-119">Electronic Business Cards</span></span>](electronic-business-cards.md)
- [<span data-ttu-id="f6aba-120">Почта</span><span class="sxs-lookup"><span data-stu-id="f6aba-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="f6aba-121">Получатели</span><span class="sxs-lookup"><span data-stu-id="f6aba-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="f6aba-122">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="f6aba-122">How Do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

