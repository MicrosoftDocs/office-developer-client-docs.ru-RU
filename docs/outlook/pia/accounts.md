---
title: Учетные записи
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: eb7c56a8a261f36628c3b440c1aeec31c7aec46e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406822"
---
# <a name="accounts"></a><span data-ttu-id="10b05-102">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="10b05-102">Accounts</span></span> 

<span data-ttu-id="10b05-103">В этом разделе представлены примеры задач, связанные с учетными записями электронной почты.</span><span class="sxs-lookup"><span data-stu-id="10b05-103">This section provides sample tasks that involve e-mail accounts.</span></span> <span data-ttu-id="10b05-104">В качестве примеров учетных записей электронной почты можно привести учетные записи Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP) и Hypertext Transfer Protocol (HTTP).</span><span class="sxs-lookup"><span data-stu-id="10b05-104">Examples of e-mail accounts are Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP), and Hypertext Transfer Protocol (HTTP) accounts.</span></span> <span data-ttu-id="10b05-105">Учетная запись для текущего профиля представлена объектом [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="10b05-105">An account for the current profile is represented by an [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) object.</span></span>


|<span data-ttu-id="10b05-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="10b05-106">Topic</span></span>|<span data-ttu-id="10b05-107">Описание</span><span class="sxs-lookup"><span data-stu-id="10b05-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="10b05-108">Получение сведений об учетной записи</span><span class="sxs-lookup"><span data-stu-id="10b05-108">Get account information</span></span>](how-to-get-account-information.md) | <span data-ttu-id="10b05-109">Принимает в качестве входного аргумента надежный объект [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) Microsoft Outlook и использует объект **Account** для отображения подробных сведений о каждой учетной записи, доступной для текущего профиля Outlook.</span><span class="sxs-lookup"><span data-stu-id="10b05-109">Takes as an input argument a trusted Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>|
|[<span data-ttu-id="10b05-110">Создание отправляемого элемента для определенной учетной записи на основе текущей папки</span><span class="sxs-lookup"><span data-stu-id="10b05-110">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | <span data-ttu-id="10b05-111">Содержит два примера кода, показывающих создание отправляемого элемента электронной почты и приглашения на собрание, а затем их отправку с использованием конкретной учетной записи на основе текущей папки.</span><span class="sxs-lookup"><span data-stu-id="10b05-111">Contains two code examples that show how to create a sendable e-mail item and meeting request, and then to send them by using a specific account that is based on the current folder.</span></span>|
|[<span data-ttu-id="10b05-112">Получение учетной записи для папки</span><span class="sxs-lookup"><span data-stu-id="10b05-112">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md) | <span data-ttu-id="10b05-113">Получение учетной записи, которая связана с папкой в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="10b05-113">Gets the account that is associated with a folder in the current session.</span></span>|
|[<span data-ttu-id="10b05-114">Получение сведений о нескольких учетных записях</span><span class="sxs-lookup"><span data-stu-id="10b05-114">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md) | <span data-ttu-id="10b05-115">Получение и отображение различных сведений о каждой учетной записи текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="10b05-115">Obtains and displays miscellaneous information about each account in the current profile.</span></span>|
|<span data-ttu-id="10b05-116">[Отправка почтового элемента с помощью учетной записи Hotmail](how-to-send-a-mail-item-by-using-a-hotmail-account.md)</span><span class="sxs-lookup"><span data-stu-id="10b05-116">Uses the [SendUsingAccount](how-to-send-a-mail-item-by-using-a-hotmail-account.md) property to send a mail item by using a Windows Live Hotmail account.</span></span> | <span data-ttu-id="10b05-117">Использование свойства [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) для отправки почтового элемента с помощью учетной записи Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="10b05-117">Uses the [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) property to send a mail item by using a Windows Live Hotmail account.</span></span>|

## <a name="see-also"></a><span data-ttu-id="10b05-118">См. также</span><span class="sxs-lookup"><span data-stu-id="10b05-118">See also</span></span>

- [<span data-ttu-id="10b05-119">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="10b05-119">Exchange Users</span></span>](exchange-users.md)
- [<span data-ttu-id="10b05-120">Почта</span><span class="sxs-lookup"><span data-stu-id="10b05-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="10b05-121">Получатели</span><span class="sxs-lookup"><span data-stu-id="10b05-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="10b05-122">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="10b05-122">How Do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

