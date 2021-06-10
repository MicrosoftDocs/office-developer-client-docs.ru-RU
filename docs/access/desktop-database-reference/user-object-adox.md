---
title: Объект пользователя (ADOX — ссылка на базу данных для настольных компьютеров)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313162"
---
# <a name="user-object-adox"></a>Объект пользователя (ADOX)


**Область применения**: Access 2013, Office 2013

Представляет учетную запись пользователя с разрешениями доступа в защищенной базе данных.

## <a name="remarks"></a>Примечания

Коллекция ["Пользователи](users-collection-adox.md) [каталога"](catalog-object-adox.md) представляет всех пользователей каталога. Коллекция **Пользователей** для [группы](group-object-adox.md) представляет только пользователей определенной группы.

С помощью свойств, коллекций и методов объекта **Пользователя** можно:

  - Определите пользователя с [свойством Name.](name-property-adox.md)

  - Измените пароль для пользователя методом [ChangePassword.](changepassword-method-adox.md)

  - Определите, читал ли пользователь, писал или удалял разрешения с помощью методов [GetPermissions](getpermissions-method-adox.md) и [SetPermissions.](setpermissions-method-adox.md)

  - Доступ к группам, к которым принадлежит пользователь в коллекции [Groups.](groups-collection-adox.md)

  - Доступ к свойствам, определенным поставщикам, с [коллекцией свойств.](properties-collection-ado.md)

