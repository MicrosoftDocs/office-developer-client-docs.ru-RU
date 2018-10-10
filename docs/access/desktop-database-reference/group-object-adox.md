---
title: Group Object (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21caab66c16c4ca9f77c49f33bf99f4df7be79c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482173"
---
# <a name="group-object-adox"></a>Group Object (ADOX)


**Применимо к**: Access 2013 | Office 2013

Представляет учетную запись группы, имеющей разрешения на доступ в рамках защищенной базы данных.

## <a name="remarks"></a>Замечания

Коллекция [групп](groups-collection-adox.md) [каталога](catalog-object-adox.md) представляет учетные записи групп каталога. Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.

С помощью свойства, семейств сайтов и методы объекта **группы** можно:

  - Идентификация группы с помощью свойства [Name](name-property-adox.md) .

  - Определите, будет ли группы имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .

  - Доступ к учетные записи пользователей, для которых членство в группе с помощью коллекции [пользователей](users-collection-adox.md) .

  - Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .

