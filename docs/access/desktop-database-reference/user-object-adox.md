---
title: Объект пользователя (ADOX - ссылки для настольных баз данных Access)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 845697f54ea5e37e051836896b84d8a3ff061237
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919882"
---
# <a name="user-object-adox"></a>Объект User (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет учетную запись пользователя, который имеет разрешения на доступ в рамках защищенной базы данных.

## <a name="remarks"></a>Примечания

Коллекция [пользователей](users-collection-adox.md) из [каталога](catalog-object-adox.md) представляет каталога пользователей. Коллекция **пользователей** для [группы](group-object-adox.md) представляет только пользователи конкретную группу.

С помощью свойства, семейств сайтов и методы объекта **пользователя** можно выполнить следующие действия.

  - Определите пользователя с помощью свойства [Name](name-property-adox.md) .

  - Изменение пароля для пользователя с помощью метода [Изменение пароля](changepassword-method-adox.md) .

  - Определить, является ли пользователь имеет чтение, запись и удаление разрешений с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions](setpermissions-method-adox.md) .

  - Доступ к групп, к которым принадлежит пользователь с коллекцией [групп](groups-collection-adox.md) .

  - Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .

