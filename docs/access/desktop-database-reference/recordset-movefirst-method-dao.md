---
title: Метод Recordset.MoveFirst (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 31d003d7ae98bf509aca8f24da9c37f0276af6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300240"
---
# <a name="recordsetmovefirst-method-dao"></a>Метод Recordset.MoveFirst (DAO)


**Область применения**: Access 2013, Office 2013

Выполняет перемещение к первой записи в указанном объекте **Recordset** и делает запись текущей.

## <a name="syntax"></a>Синтаксис

*expression* .MoveFirst

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Комментарии

Используйте методы **Move**, чтобы перейти от записи к записи, не применяя условие.

Если вы редактируете текущую запись, убедитесь, что вы используете метод **Update**, чтобы сохранить изменения, перед переходом к другой записи. Если перейти к другой записи без обновления, изменения будут потеряны без предупреждения.

Когда вы открываете **Recordset**, первую запись является текущей, а свойство **BOF** имеет значение **False**. Если **Recordset** не содержит записей, свойство **BOF** имеет значение **True**, а текущая запись отсутствует.

Если первая или последняя запись уже является текущей при использовании **MoveFirst** или **MoveLast**, текущая запись не меняется.

Если recordset указывает на табличный тип объекта **Recordset** (только для рабочих областей Microsoft Access), перемещение отвечает текущему индексу. Вы можете задать текущий индекс с помощью свойства **Index**. Если не задать текущей индекс, порядок возвращаемых записей будет не определен.

Вы не можете использовать методы **MoveFirst**, **MoveLast** и **MovePrevious** для объекта **Recordset** однонаправленного типа.

Чтобы переместить положение текущей записи в объекте **Recordset** на определенное количество записей вперед или назад, используйте метод **Move**.

