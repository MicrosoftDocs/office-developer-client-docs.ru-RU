---
title: Удаление метода (ADOX коллекций)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708636"
---
# <a name="delete-method-adox-collections"></a>Удаление метода (ADOX коллекций)

**Применимо к**: Access 2013, Office 2013

Удаляет объект из коллекции.

## <a name="syntax"></a>Синтаксис

*Семейства сайтов*. Удалите*имя*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Name* |**Variant** , которое указывает имя или порядковый номер (индекс) объекта для удаления.|

## <a name="remarks"></a>Замечания

Если *имя* не существует в коллекции, произойдет ошибка.

Для коллекций [таблиц](tables-collection-adox.md) и [пользователей](users-collection-adox.md) Если поставщик поддерживает удаление таблицы или пользователей, соответственно, произойдет ошибка. Для коллекций, [представления](views-collection-adox.md) и [процедуры](procedures-collection-adox.md) **удалите** завершится ошибкой, если поставщик не поддерживает сохранение команды.

