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
# <a name="accounts"></a>Учетные записи 

В этом разделе представлены примеры задач, связанные с учетными записями электронной почты. В качестве примеров учетных записей электронной почты можно привести учетные записи Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP) и Hypertext Transfer Protocol (HTTP). Учетная запись для текущего профиля представлена объектом [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia).


|Раздел|Описание|
|:----|:----------|
|[Получение сведений об учетной записи](how-to-get-account-information.md) | Принимает в качестве входного аргумента надежный объект [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) Microsoft Outlook и использует объект **Account** для отображения подробных сведений о каждой учетной записи, доступной для текущего профиля Outlook.|
|[Создание отправляемого элемента для определенной учетной записи на основе текущей папки](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | Содержит два примера кода, показывающих создание отправляемого элемента электронной почты и приглашения на собрание, а затем их отправку с использованием конкретной учетной записи на основе текущей папки.|
|[Получение учетной записи для папки](how-to-get-the-account-for-a-folder.md) | Получение учетной записи, которая связана с папкой в текущем сеансе.|
|[Получение сведений о нескольких учетных записях](how-to-get-information-about-multiple-accounts.md) | Получение и отображение различных сведений о каждой учетной записи текущего профиля.|
|[Отправка почтового элемента с помощью учетной записи Hotmail](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | Использование свойства [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) для отправки почтового элемента с помощью учетной записи Windows Live Hotmail.|

## <a name="see-also"></a>См. также

- [Пользователи Exchange](exchange-users.md)
- [Почта](mail.md)
- [Получатели](recipients.md)
- [Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

