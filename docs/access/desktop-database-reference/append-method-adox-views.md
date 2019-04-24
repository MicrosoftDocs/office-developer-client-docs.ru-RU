---
title: Метод Append (Views в ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297048"
---
# <a name="append-method-adox-views"></a>Метод Append (Views в ADOX)

**Область применения**: Access 2013, Office 2013

Создает новый объект [View](view-object-adox.md) и добавляет его в коллекцию views [](views-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Представления*. *Имя*для добавления, *команда*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |**Строковое** значение, задающее имя создаваемого представления.|
|*Command* |Объект [команды](command-object-ado.md) ADO, представляющий представление, которое требуется создать.|

## <a name="remarks"></a>Замечания

Создает новое представление в источнике данных с именем и атрибутами, указанными в объекте **Command** .

Если текст команды, который указывает пользователь, представляет процедуру, а не представление, поведение зависит от поставщика. Если поставщик не поддерживает хранимые команды, **append** завершится с ошибками.

> [!NOTE]
> При использовании поставщика OLE DB для Microsoft Jet метод **append** коллекции **views** позволяет указать **процедуру** , а не **представление** в параметре *Command* . **Процедура** будет добавлена в источник данных и будет добавлена в коллекцию **views** . После **добавления**, если коллекции **процедур** и **представлений** обновляются, **процедура** больше не будет находиться в коллекции Views и будет отображаться **** в коллекции **процедур** .


