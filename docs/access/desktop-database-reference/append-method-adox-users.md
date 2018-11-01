---
title: Добавьте метод (ADOX пользователей)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 948ba15ccca5dabe6b4cb75c09f7e47e65994b2b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887770"
---
# <a name="append-method-adox-users"></a>Добавьте метод (ADOX пользователей)


**Применимо к**: Access 2013, Office 2013


Добавляет новый объект [пользователя](user-object-adox.md) в коллекции [пользователей](users-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Пользователи*. Добавление*пользователя*\[,*пароль*\]

## <a name="parameters"></a>Параметры

  - *user*

  - Значение **типа Variant** , содержащее объект **пользователя** для добавления или имя пользователя для создания и добавления.

  - *Password*

  - Необязательный параметр. **Строковое** значение, содержащее пароль для пользователя. Параметр *Password* соответствует значению, указанному с помощью метода [Изменение пароля](changepassword-method-adox.md) объекта **пользователя** .

## <a name="remarks"></a>Замечания

Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей. Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.

Если поставщик не поддерживает создание пользователей, произойдет ошибка.


> [!NOTE]
> Перед добавлением объекта **пользователя** в коллекцию **пользователей** объекта **группы** , объект **пользователя** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекции **пользователей** из **каталога**.


