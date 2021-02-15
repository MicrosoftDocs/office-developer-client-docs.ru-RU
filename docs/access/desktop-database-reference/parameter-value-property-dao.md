---
title: Свойство Parameter.Value (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4e7f3976b934c407a038f321953259fd63a6f60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287994"
---
# <a name="parametervalue-property-dao"></a>Свойство Parameter.Value (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение объекта. Для чтения и записи, **Variant**.

## <a name="syntax"></a>Синтаксис

*выражение .* Значение

*выражение* Переменная, представляюная объект **Parameter.**

## <a name="remarks"></a>Заметки

Значение параметра или возвращаемого значения — это тип данных Variant, который оценивается как значение, подходящее для типа данных, как указано в свойстве **Type** объекта.

Как правило, свойство **Value** используется для извлечения и изменения данных в **объектах Recordset.**

Свойство **Value** является свойством по умолчанию для объектов **Field,** **Parameter** и **Property.** Поэтому можно задать или вернуть значение одного из этих объектов, ссылаясь на них напрямую, а не на свойство **Value.**

Попытка установить или вернуть свойство **Value** в недопустимом контексте (например, свойство **Value** объекта **Field** в коллекции **Fields** объекта **TableDef)** приведет к перехитовке ошибки.

> [!NOTE]
> При чтении десятичных значений из базы данных Microsoft SQL Server они будут отформатированы с использованием нотации в рабочей области Microsoft Access, но будут отображаться как обычные десятичные значения в рабочей области ODBCDirect.


