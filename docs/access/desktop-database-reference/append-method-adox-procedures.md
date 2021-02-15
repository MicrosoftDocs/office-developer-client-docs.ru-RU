---
title: Метод Append (коллекция Procedures в ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297083"
---
# <a name="append-method-adox-procedures"></a>Метод Append (коллекция Procedures в ADOX)

**Область применения**: Access 2013, Office 2013

Добавляет новый [объект Procedure](procedure-object-adox.md) в [коллекцию Procedures.](procedures-collection-adox.md)

## <a name="syntax"></a>Синтаксис

*Процедуры*. Имя *приложения*, *команда*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |**Строка,** задав имя создаемой и добавленной процедуры.|
|*Command* |Объект команды [ADO,](command-object-ado.md) который представляет процедуру для создания и приложения.|

## <a name="remarks"></a>Заметки

Создает новую процедуру в источнике данных с именем и атрибутами, указанными в **объекте Command.**

Если заданный пользователем текст команды представляет представление, а не процедуру, поведение зависит от используемого поставщика. **Приложение не** будет работать, если поставщик не поддерживает сохраняющиеся команды.

> [!NOTE]
> При использовании поставщика OLE DB для Microsoft Jet метод **Append** коллекции  **Procedures** позволяет  указать представление, а не процедуру в параметре *Command.* Представление **будет** добавлено в источник данных и добавлено в коллекцию **процедур.** После обновления **коллекций "Append"**  и **"Просмотры"** представление больше не будет в коллекции **Procedures** и будет отображаться в коллекции  **Views.**


