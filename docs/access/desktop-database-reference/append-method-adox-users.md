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

Добавляет новый объект [User](user-object-adox.md) в коллекцию [Users](users-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Пользователи*. Добавление*пользователя*\[,*пароль*\]

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Пользователь* |Значение **Variant** , содержащее объект **пользователя** для добавления или имя пользователя, для которого создается и добавляется.|
|*Password* |Необязательный атрибут. **Строковое** значение, содержащее пароль для пользователя. Параметр *Password* соответствует значению, указанному в методе [ChangePassword](changepassword-method-adox.md) объекта **пользователя** .|

## <a name="remarks"></a>Замечания

Коллекция **Users** [каталога](catalog-object-adox.md) Users содержит все пользователи каталога. Коллекция **Users** для [группы](group-object-adox.md) представляет только тех пользователей, у которых есть членство в определенной группе.

Если поставщик не поддерживает создание пользователей, произойдет ошибка.

> [!NOTE]
> Перед добавлением объекта **User** в коллекцию **Users** объекта **Group** объект **пользователя** с тем же [именем](name-property-adox.md) , что и у добавляемОго объекта, должен уже существовать в коллекции Users **каталога**. ****


