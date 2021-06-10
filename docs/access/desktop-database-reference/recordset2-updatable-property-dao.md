---
title: Свойство Recordset2.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b6e6f2a20b4779259b80eff1fc152abe3698217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309326"
---
# <a name="recordset2updatable-property-dao"></a>Свойство Recordset2.Updatable (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает на то, можно ли изменить DAO объект. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражения* . Updatable

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Примечания

Объекты Recordset с мгновенными снимками и только для форвардного типа всегда возвращают **false**.

Многие типы объектов могут содержать поля, которые не могут быть обновлены. Например, можно создать объект **Recordset** типа dynaset, в котором можно изменить только некоторые поля. Эти поля могут быть исправлены или содержать данные, которые автоматически прибавления, или dynaset может быть результатом запроса, который объединяет updatable и nonupdatable таблицы.

Если объект содержит только поля только для чтения, значение свойства **Updatable** **false**. Если одно или несколько полей являются updatable, значение свойства **True**. Можно редактировать только updatable fields. При попытке назначить новое значение в поле только для чтения возникает ошибка.

Так как updatable объект может содержать поля только для чтения, перед редактированием записи проверьте свойство **DataUpdatable** для каждого поля в коллекции **Полей** объекта **Recordset.**

