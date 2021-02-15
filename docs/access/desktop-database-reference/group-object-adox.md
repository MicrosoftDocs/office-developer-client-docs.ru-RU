---
title: Объект Group (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e010ac58ff0b573d42c562ce3be7a99acab5abea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292120"
---
# <a name="group-object-adox"></a>Объект Group (ADOX)


**Область применения**: Access 2013, Office 2013

Представляет учетную запись группы, которая имеет разрешения на доступ в защищенной базе данных.

## <a name="remarks"></a>Заметки

Коллекция [Groups](groups-collection-adox.md) [каталога представляет](catalog-object-adox.md) все учетные записи группы каталога. Коллекция **Groups** для [пользователя представляет](user-object-adox.md) только группу, к которой принадлежит пользователь.

С помощью свойств, коллекций и методов объекта **Group** можно:

  - Определите группу с помощью [свойства Name.](name-property-adox.md)

  - Определите, имеет ли группа разрешения на чтение, запись или удаление с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions.](setpermissions-method-adox.md)

  - Доступ к учетным записям пользователей, которые имеют членство в группе, в коллекции [Users.](users-collection-adox.md)

  - Доступ к свойствам поставщика с помощью коллекции [Properties.](properties-collection-ado.md)

