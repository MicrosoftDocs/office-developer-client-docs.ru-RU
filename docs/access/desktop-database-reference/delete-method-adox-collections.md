---
title: Метод удаления (коллекции ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294080"
---
# <a name="delete-method-adox-collections"></a>Метод удаления (коллекции ADOX)

**Область применения**: Access 2013, Office 2013

Удаляет объект из коллекции.

## <a name="syntax"></a>Синтаксис

*Коллекция*. Удаление *имени*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |**Вариант,** который указывает имя или координатную позицию (индекс) объекта для удаления.|

## <a name="remarks"></a>Примечания

Ошибка произойдет, если *имя* не существует в коллекции.

Для [коллекций](tables-collection-adox.md) [Таблицы](users-collection-adox.md) и Пользователи возникает ошибка, если поставщик не поддерживает удаление таблиц или пользователей соответственно. Для [коллекций "Процедуры](procedures-collection-adox.md) и [представления"](views-collection-adox.md) **удаление** не удастся, если поставщик не поддерживает сохраняющиеся команды.

