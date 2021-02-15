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

Создает новый объект [View](view-object-adox.md) и включает его в [коллекцию Views.](views-collection-adox.md)

## <a name="syntax"></a>Синтаксис

*Представления*. Имя *приложения*, *команда*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |**Строка,** которая указывает имя создаемого представления.|
|*Command* |Объект команды [ADO,](command-object-ado.md) представляю собой представление, которое необходимо создать.|

## <a name="remarks"></a>Заметки

Создает новое представление в источнике данных с именем и атрибутами, указанными в **объекте Command.**

Если заданный пользователем текст команды представляет процедуру, а не представление, поведение зависит от поставщика. **Приложение не** будет работать, если поставщик не поддерживает сохраняющиеся команды.

> [!NOTE]
> При использовании поставщика OLE DB для Microsoft Jet метод  **Append** коллекции  **Views** позволяет указать в параметре *Command* процедуру, а не представление. Процедура **будет** добавлена в источник данных и добавлена в коллекцию **Views.** После обновления коллекций  "Append" и **"Procedures** and **Views"** процедура больше не будет в коллекции **Views** и будет отображаться в коллекции  **Procedures.**


