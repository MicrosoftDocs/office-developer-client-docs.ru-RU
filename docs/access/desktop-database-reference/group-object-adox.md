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

Представляет учетную запись группы, имеющую разрешения на доступ в защищенной базе данных.

## <a name="remarks"></a>Примечания

Коллекция [Groups](groups-collection-adox.md) [каталога](catalog-object-adox.md) представляет все учетные записи групп в каталоге. Коллекция **Groups** для [пользователя](user-object-adox.md) представляет только группу, к которой принадлежит пользователь.

С помощью свойств, коллекций и методов объекта **Group** можно выполнять следующие действия:

  - Определите группу с помощью свойства [Name](name-property-adox.md) .

  - Определите, имеет ли группа разрешения на чтение, запись или удаление [с помощью методов](getpermissions-method-adox.md) [SetPermissions](setpermissions-method-adox.md) и.

  - Доступ к учетным записям пользователей с членством в группе с коллекцией [Users](users-collection-adox.md) .

  - Доступ к свойствам, зависящим от поставщика, с коллекцией [свойств](properties-collection-ado.md) .

