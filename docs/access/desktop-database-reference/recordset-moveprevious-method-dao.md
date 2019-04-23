---
title: Метод Recordset.MovePrevious (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 82a3bc3e-5221-9a1a-1350-47bc6759edeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196699(v=office.15)
ms:contentKeyID: 48545984
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052872
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 95cf5daa9eac6644b17f47b09ebc749bd9ed928e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284513"
---
# <a name="recordsetmoveprevious-method-dao"></a>Метод Recordset.MovePrevious (DAO)


**Область применения**: Access 2013, Office 2013

Выполняет перемещение к предыдущей записи в указанном объекте **Recordset** и делает запись текущей.

## <a name="syntax"></a>Синтаксис

*Expression* . MovePrevious

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Комментарии

Используйте методы **Move**, чтобы перейти от записи к записи, не применяя условие.

Если вы редактируете текущую запись, убедитесь, что вы используете метод **Update**, чтобы сохранить изменения, перед переходом к другой записи. Если перейти к другой записи без обновления, изменения будут потеряны без предупреждения.

Когда вы открываете **Recordset**, первую запись является текущей, а свойство **BOF** имеет значение **False**. Если **Recordset** не содержит записей, свойство **BOF** имеет значение **True**, а текущая запись отсутствует.

Если используется **MovePrevious** , когда первая запись является текущей, свойство **BOF** имеет **значение true**, а текущая запись отсутствует. При повторном использовании **MovePrevious** возникает ошибка, и **BOF** остается **true**.

Если recordset указывает на табличный тип объекта **Recordset** (только для рабочих областей Microsoft Access), перемещение отвечает текущему индексу. Вы можете задать текущий индекс с помощью свойства **Index**. Если не задать текущей индекс, порядок возвращаемых записей будет не определен.

Вы не можете использовать методы **MoveFirst**, **MoveLast** и **MovePrevious** для объекта **Recordset** однонаправленного типа.

Чтобы переместить положение текущей записи в объекте **Recordset** на определенное количество записей вперед или назад, используйте метод **Move**.

