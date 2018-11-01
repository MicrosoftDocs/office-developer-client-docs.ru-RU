---
title: Объект группы (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f98e65522ebefdb8f3897234d04e54d9599dda
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883682"
---
# <a name="group-object-adox"></a>Объект группы (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет учетную запись группы, имеющей разрешения на доступ в рамках защищенной базы данных.

## <a name="remarks"></a>Замечания

Коллекция [групп](groups-collection-adox.md) [каталога](catalog-object-adox.md) представляет учетные записи групп каталога. Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.

С помощью свойства, семейств сайтов и методы объекта **группы** можно:

  - Идентификация группы с помощью свойства [Name](name-property-adox.md) .

  - Определите, будет ли группы имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .

  - Доступ к учетные записи пользователей, для которых членство в группе с помощью коллекции [пользователей](users-collection-adox.md) .

  - Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .

