---
title: Свойство Field2.Value (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4324917fcabd768a9527b11fceadbfc2dc9ef2b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292631"
---
# <a name="field2value-property-dao"></a>Свойство Field2.Value (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение объекта. Для чтения и записи, **Variant**.

## <a name="syntax"></a>Синтаксис

*выражение .* Значение

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Заметки

Значение параметра или возвращаемого значения — это тип данных Variant, который оценивается как значение, соответствующее типу данных, как указано в свойстве **Type** объекта.

Как правило, свойство **Value** используется для извлечения и изменения данных в **объектах Recordset.**

Свойство **Value** является свойством по умолчанию объектов **Field2,** **Parameter** и **Property.** Поэтому можно задать или вернуть значение одного из этих объектов, ссылаясь на них напрямую, а не на свойство **Value.**

Попытка установить или вернуть свойство **Value** в недопустимом контексте (например, свойство **Value** объекта **Field2** в коллекции **Fields** объекта **TableDef)** приведет к перехитовке ошибки.


> [!NOTE]
> При чтении десятичных значений из базы данных Microsoft SQL Server они будут отформатированы с использованием нотации в рабочей области Microsoft Access, но будут отображаться как обычные десятичные значения в рабочей области ODBCDirect.


