---
title: Delete Method (ADOX Collections)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea02f02270649783873f1f086bb9f39b804034a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482697"
---
# <a name="delete-method-adox-collections"></a>Delete Method (ADOX Collections)


**Применимо к**: Access 2013 | Office 2013



Удаляет объект из коллекции.

## <a name="syntax"></a>Синтаксис

*Семейства сайтов*. Удалите*имя*

## <a name="parameters"></a>Параметры

  - *Имя*

  - **Variant** , которое указывает имя или порядковый номер (индекс) объекта для удаления.

## <a name="remarks"></a>Замечания

Если *имя* не существует в коллекции, произойдет ошибка.

Для коллекций [таблиц](tables-collection-adox.md) и [пользователей](users-collection-adox.md) Если поставщик поддерживает удаление таблицы или пользователей, соответственно, произойдет ошибка. Для коллекций, [представления](views-collection-adox.md) и [процедуры](procedures-collection-adox.md) **удалите** завершится ошибкой, если поставщик не поддерживает сохранение команды.

