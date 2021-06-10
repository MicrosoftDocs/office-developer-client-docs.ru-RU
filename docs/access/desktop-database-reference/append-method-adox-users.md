---
title: Метод Append (коллекция Users в ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297069"
---
# <a name="append-method-adox-users"></a>Метод Append (коллекция Users в ADOX)

**Область применения**: Access 2013, Office 2013

Добавляет новый [объект User](user-object-adox.md) в коллекцию [Пользователей.](users-collection-adox.md)

## <a name="syntax"></a>Синтаксис

*Пользователи*. Пользователь *приложения* \[ ,*пароль*\]

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Пользователь* |Значение **Variant,** содержаное объект **Пользователя** для приложения или имя пользователя для создания и приложения.|
|*Password* |Необязательный параметр. Значение **String,** содержа которое содержит пароль для пользователя. Параметр *Password* соответствует значению, указанному методом [ChangePassword](changepassword-method-adox.md) объекта **Пользователя.**|

## <a name="remarks"></a>Примечания

Коллекция **"Пользователи** [каталога"](catalog-object-adox.md) представляет всех пользователей каталога. Коллекция **Пользователей** для [группы представляет](group-object-adox.md) только пользователей, которые имеют членство в определенной группе.

Ошибка произойдет, если поставщик не поддерживает создание пользователей.

> [!NOTE]
> Прежде чем примковать  объект Пользователя к коллекции  Пользователей объекта **Group,** объект User с тем же именем, что и объект, который должен быть придан, уже должен существовать в коллекции **Пользователей**  **каталога.** [](name-property-adox.md)


