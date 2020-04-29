---
title: Учетные записи
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d539f38419a8eaac60cd3054da6283a49bf4cc00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331187"
---
# <a name="accounts"></a><span data-ttu-id="0da0d-102">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="0da0d-102">Accounts</span></span> 

<span data-ttu-id="0da0d-103">В этом разделе представлены примеры задач, связанные с учетными записями электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0da0d-103">This section provides sample tasks that involve email accounts.</span></span> <span data-ttu-id="0da0d-104">В качестве примеров учетных записей электронной почты можно привести учетные записи Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP) и Hypertext Transfer Protocol (HTTP).</span><span class="sxs-lookup"><span data-stu-id="0da0d-104">Examples of email accounts are Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP), and Hypertext Transfer Protocol (HTTP) accounts.</span></span> <span data-ttu-id="0da0d-105">Учетная запись для текущего профиля представлена объектом [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="0da0d-105">An account for the current profile is represented by an [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) object.</span></span>


|<span data-ttu-id="0da0d-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="0da0d-106">Topic</span></span>|<span data-ttu-id="0da0d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0da0d-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="0da0d-108">Получение сведений об учетной записи</span><span class="sxs-lookup"><span data-stu-id="0da0d-108">Get account information</span></span>](how-to-get-account-information.md) | <span data-ttu-id="0da0d-109">Принимает в качестве входного аргумента надежный объект [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) Microsoft Outlook и использует объект **Account** для отображения подробных сведений о каждой учетной записи, доступной для текущего профиля Outlook.</span><span class="sxs-lookup"><span data-stu-id="0da0d-109">Takes as an input argument a trusted Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>|
|[<span data-ttu-id="0da0d-110">Создание отправляемого элемента для определенной учетной записи на основе текущей папки</span><span class="sxs-lookup"><span data-stu-id="0da0d-110">Create a sendable item for a specific account based on the current folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | <span data-ttu-id="0da0d-111">Содержит два примера кода, показывающих создание отправляемого элемента электронной почты и приглашения на собрание, а затем их отправку с использованием конкретной учетной записи на основе текущей папки.</span><span class="sxs-lookup"><span data-stu-id="0da0d-111">Contains two code examples that show how to create a sendable email item and meeting request, and then send them by using a specific account that is based on the current folder.</span></span>|
|[<span data-ttu-id="0da0d-112">Получение учетной записи для папки</span><span class="sxs-lookup"><span data-stu-id="0da0d-112">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md) | <span data-ttu-id="0da0d-113">Получение учетной записи, которая связана с папкой в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="0da0d-113">Gets the account that is associated with a folder in the current session.</span></span>|
|[<span data-ttu-id="0da0d-114">Получение сведений о нескольких учетных записях</span><span class="sxs-lookup"><span data-stu-id="0da0d-114">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md) | <span data-ttu-id="0da0d-115">Получение и отображение различных сведений о каждой учетной записи текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="0da0d-115">Obtains and displays miscellaneous information about each account in the current profile.</span></span>|
|[<span data-ttu-id="0da0d-116">Отправка почтового элемента с помощью учетной записи Hotmail</span><span class="sxs-lookup"><span data-stu-id="0da0d-116">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | <span data-ttu-id="0da0d-117">Использование свойства [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) для отправки почтового элемента с помощью учетной записи Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="0da0d-117">Uses the [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) property to send a mail item by using a Windows Live Hotmail account.</span></span>|

## <a name="see-also"></a><span data-ttu-id="0da0d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0da0d-118">See also</span></span>

- [<span data-ttu-id="0da0d-119">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="0da0d-119">Exchange users</span></span>](exchange-users.md)
- [<span data-ttu-id="0da0d-120">Почта</span><span class="sxs-lookup"><span data-stu-id="0da0d-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="0da0d-121">Получатели</span><span class="sxs-lookup"><span data-stu-id="0da0d-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="0da0d-122">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="0da0d-122">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

