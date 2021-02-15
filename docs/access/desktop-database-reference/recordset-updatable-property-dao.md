---
title: Свойство Recordset.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 722ccc2334cd00ed89a1193709023db039ba9fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307548"
---
# <a name="recordsetupdatable-property-dao"></a>Свойство Recordset.Updatable (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает на то, можно ли изменить DAO объект. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение .* Updatable

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Объекты Recordset типа "моментальный снимок" и "только для переад/ всегда возвращают **false"**.

Многие типы объектов могут содержать поля, которые не могут быть обновлены. Например, можно создать объект **Recordset** типа dynaset, в котором можно изменить только некоторые поля. Эти поля могут быть исправлены или содержать данные, которые автоматически приращены, или набор dynaset может быть результатом запроса, объединяющего неустанные и неустандартные таблицы.

Если объект содержит только поля только для чтения, свойство **Updatable** имеет значение **False.** Если одно или несколько полей могут быть updatable, свойство имеет значение **True**. Можно редактировать только поля, которые можно изменить. Если попытаться назначить новое значение только для чтения, возникает перехитиемая ошибка.

Так как updatable объект может содержать поля только для чтения, перед редактированием записи проверьте свойство **DataUpdatable** каждого поля в коллекции **Fields** объекта **Recordset.**

