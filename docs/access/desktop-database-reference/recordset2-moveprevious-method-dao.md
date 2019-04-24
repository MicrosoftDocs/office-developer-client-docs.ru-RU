---
title: Метод Recordset2. MovePrevious (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9753d3bbb586e2c1bd44755deb529758d8eab060
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307247"
---
# <a name="recordset2moveprevious-method-dao"></a>Метод Recordset2. MovePrevious (DAO)


**Область применения**: Access 2013, Office 2013

Выполняет перемещение к предыдущей записи в указанном объекте **Recordset** и делает запись текущей.

## <a name="syntax"></a>Синтаксис

*Expression* . MovePrevious

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Комментарии

Используйте методы **Move**, чтобы перейти от записи к записи, не применяя условие.

Если вы редактируете текущую запись, убедитесь, что вы используете метод **Update**, чтобы сохранить изменения, перед переходом к другой записи. Если перейти к другой записи без обновления, изменения будут потеряны без предупреждения.

Когда вы открываете **Recordset**, первую запись является текущей, а свойство **BOF** имеет значение **False**. Если **Recordset** не содержит записей, свойство **BOF** имеет значение **True**, а текущая запись отсутствует.

Если используется **MovePrevious** , когда первая запись является текущей, свойство **BOF** имеет **значение true**, а текущая запись отсутствует. При повторном использовании **MovePrevious** возникает ошибка, и **BOF** остается **true**.

Если recordset указывает на табличный тип объекта **Recordset** (только для рабочих областей Microsoft Access), перемещение отвечает текущему индексу. Вы можете задать текущий индекс с помощью свойства **Index**. Если не задать текущей индекс, порядок возвращаемых записей будет не определен.

Вы не можете использовать методы **MoveFirst**, **MoveLast** и **MovePrevious** для объекта **Recordset** однонаправленного типа.

Чтобы переместить положение текущей записи в объекте **Recordset** на определенное количество записей вперед или назад, используйте метод **Move**.

