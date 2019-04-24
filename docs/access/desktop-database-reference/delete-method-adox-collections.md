---
title: Метод Delete (коллекции ADOX)
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
# <a name="delete-method-adox-collections"></a>Метод Delete (коллекции ADOX)

**Область применения**: Access 2013, Office 2013

Удаляет объект из коллекции.

## <a name="syntax"></a>Синтаксис

*Коллекция*. Удаление*имени*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |**Значение Variant** , задающее имя или порядковый номер объекта, который требуется удалить.|

## <a name="remarks"></a>Замечания

Если *имя* не существует в коллекции, произойдет ошибка.

Для коллекций [таблиц](tables-collection-adox.md) и [пользователей](users-collection-adox.md) возникает ошибка, если поставщик не поддерживает удаление таблиц или пользователей соответственно. Для коллекций [процедур](procedures-collection-adox.md) и [представлений](views-collection-adox.md) **Удаление** завершится с ошибками, если поставщик не поддерживает хранимые команды.

