---
title: View Object (ADOX - Access desktop database reference)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306051"
---
# <a name="view-object-adox"></a>Объект View (ADOX)


**Область применения**: Access 2013, Office 2013

Представляет отфильтрованный набор записей или виртуальную таблицу. При использовании в сочетании с объектом ADO [Command](command-object-ado.md) объект **View** можно использовать для добавления, удаления или изменения представлений.

## <a name="remarks"></a>Заметки

Представление — это виртуальная таблица, созданная из других таблиц или представлений базы данных. Объект **View** позволяет создавать представление без необходимости знать или использовать синтаксис "CREATE VIEW" поставщика.

С помощью свойств объекта **View** можно:

  - Определите представление с помощью [свойства Name.](name-property-adox.md)

  - Укажите объект **команды** ADO, который можно использовать для добавления, удаления или изменения представлений с помощью свойства [Command.](command-property-adox.md)

  - Сведения о дате возврата [со свойствами DateCreated](datecreated-property-adox.md) и [DateModified.](datemodified-property-adox.md)

