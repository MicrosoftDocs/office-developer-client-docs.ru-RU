---
title: Метод Append (коллекция Users в ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf855fc6e829ebfbe3809925bf1ab8ca337d3f96
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949413"
---
# <a name="append-method-adox-users"></a>Метод Append (коллекция Users в ADOX)

**Применимо к**: Access 2013, Office 2013

Добавляет новый объект [пользователя](user-object-adox.md) в коллекции [пользователей](users-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Пользователи*. Добавление*пользователя*\[,*пароль*\]

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*user* |Значение **типа Variant** , содержащее объект **пользователя** для добавления или имя пользователя для создания и добавления.|
|*Password* |Необязательно указывать. **Строковое** значение, содержащее пароль для пользователя. Параметр *Password* соответствует значению, указанному с помощью метода [Изменение пароля](changepassword-method-adox.md) объекта **пользователя** .|

## <a name="remarks"></a>Примечания

Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей. Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.

Если поставщик не поддерживает создание пользователей, произойдет ошибка.

> [!NOTE]
> Перед добавлением объекта **пользователя** в коллекцию **пользователей** объекта **группы** , объект **пользователя** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекции **пользователей** из **каталога**.


