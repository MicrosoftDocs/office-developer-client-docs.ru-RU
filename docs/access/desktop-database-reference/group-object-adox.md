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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718170"
---
# <a name="group-object-adox"></a>Объект Group (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет учетную запись группы, имеющей разрешения на доступ в рамках защищенной базы данных.

## <a name="remarks"></a>Замечания

Коллекция [групп](groups-collection-adox.md) [каталога](catalog-object-adox.md) представляет учетные записи групп каталога. Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.

С помощью свойства, семейств сайтов и методы объекта **группы** можно:

  - Идентификация группы с помощью свойства [Name](name-property-adox.md) .

  - Определите, будет ли группы имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .

  - Доступ к учетные записи пользователей, для которых членство в группе с помощью коллекции [пользователей](users-collection-adox.md) .

  - Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .

