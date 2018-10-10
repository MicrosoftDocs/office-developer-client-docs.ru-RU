---
title: Append Method (ADOX Users)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480569"
---
# <a name="append-method-adox-users"></a>Append Method (ADOX Users)


**Применимо к**: Access 2013 | Office 2013


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
> <P>Перед добавлением объекта <STRONG>пользователя</STRONG> в коллекцию <STRONG>пользователей</STRONG> объекта <STRONG>группы</STRONG> , объект <STRONG>пользователя</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекции <STRONG>пользователей</STRONG> из <STRONG>каталога</STRONG>.</P>


