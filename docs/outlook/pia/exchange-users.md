---
title: Пользователи Exchange
TOCTitle: Exchange users
ms:assetid: 01802032-fd60-400b-ad83-1f4eefe596bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184585(v=office.15)
ms:contentKeyID: 55119835
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 775bfa2c67f3f570bddc749fb995460f6b90b18a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406990"
---
# <a name="exchange-users"></a>Пользователи Exchange

В этом разделе представлены примеры задач, связанных с пользователями почтовых ящиков Microsoft Exchange. Пользователи Exchange подключаются к серверу Exchange и представлены объектами [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) , которые являются производными от объекта [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) .

## <a name="in-this-section"></a>В этой статье

|Раздел|Описание|
|:----|:----------|
|[Получение сведений о текущем пользователе](how-to-get-information-about-the-current-user.md)  |Получение сведений о текущем пользователе, например имени, должности и номера телефона.|
|[Получение сведений обо всех списках рассылки, участником которых является текущий пользователь](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)  |Получение сведений обо всех списках рассылки, участником которых является текущий пользователь, с помощью метода [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)).|
|[Создание списка рассылки](how-to-create-a-distribution-list.md)  |Создание списка рассылки и отображение его пользователю.|
[Получение участников списка рассылки Exchange](how-to-get-members-of-an-exchange-distribution-list.md)  |Приглашение пользователю указать список рассылки Exchange с помощью диалогового окна **Выбор имен** и разворачивание этого списка рассылки, чтобы отобразить его участников.|
[Получение сведений о руководителе текущего пользователя](how-to-get-information-about-the-current-user-s-manager.md)  |Получение сведений (например, имени, должности и номеров телефонов) о руководителе текущего пользователя.|
[Получение сведений о доступности для руководителя пользователя Exchange](how-to-get-availability-information-for-an-exchange-user-s-manager.md) |  Отображение следующего свободного 60-минутного интервала времени в календаре руководителя пользователя.|
|[Проверка ответа руководителя на приглашение на собрание](how-to-check-a-manager-s-response-to-a-meeting-request.md) | Проверка состояния ответа руководителя текущего пользователя на приглашение на собрание с помощью методов [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) и [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)).|
|[Получение сведений о подчиненных руководителя текущего пользователя](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md) | Получение подчиненных руководителя текущего пользователя (при наличии) и последующее отображение сведений о каждом из подчиненных руководителя.|

## <a name="see-also"></a>См. также

- [Учетные записи](accounts.md)
- [Адресная книга](address-book.md)
- [Хранилища](stores.md)
- [Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

