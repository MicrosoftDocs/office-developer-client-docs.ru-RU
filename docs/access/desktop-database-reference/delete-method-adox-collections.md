---
title: Удаление метода (ADOX коллекций)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 893890e43725d8c667ee5f72b396d3ec8947f395
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949371"
---
# <a name="delete-method-adox-collections"></a>Удаление метода (ADOX коллекций)

**Применимо к**: Access 2013, Office 2013

Удаляет объект из коллекции.

## <a name="syntax"></a>Синтаксис

*Семейства сайтов*. Удалите*имя*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |**Variant** , которое указывает имя или порядковый номер (индекс) объекта для удаления.|

## <a name="remarks"></a>Примечания

Если *имя* не существует в коллекции, произойдет ошибка.

Для коллекций [таблиц](tables-collection-adox.md) и [пользователей](users-collection-adox.md) Если поставщик поддерживает удаление таблицы или пользователей, соответственно, произойдет ошибка. Для коллекций, [представления](views-collection-adox.md) и [процедуры](procedures-collection-adox.md) **удалите** завершится ошибкой, если поставщик не поддерживает сохранение команды.

