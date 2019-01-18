---
title: Объект пользователя (ADOX - ссылки для настольных баз данных Access)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702616"
---
# <a name="user-object-adox"></a>Объект User (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет учетную запись пользователя, который имеет разрешения на доступ в рамках защищенной базы данных.

## <a name="remarks"></a>Замечания

Коллекция [пользователей](users-collection-adox.md) из [каталога](catalog-object-adox.md) представляет каталога пользователей. Коллекция **пользователей** для [группы](group-object-adox.md) представляет только пользователи конкретную группу.

С помощью свойства, семейств сайтов и методы объекта **пользователя** можно выполнить следующие действия.

  - Определите пользователя с помощью свойства [Name](name-property-adox.md) .

  - Изменение пароля для пользователя с помощью метода [Изменение пароля](changepassword-method-adox.md) .

  - Определить, является ли пользователь имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .

  - Доступ к групп, к которым принадлежит пользователь с коллекцией [групп](groups-collection-adox.md) .

  - Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .

