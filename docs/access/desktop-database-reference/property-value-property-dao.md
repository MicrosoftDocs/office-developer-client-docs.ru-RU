---
title: Свойство Property. Value (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e7c79fe12b3b7bfe98e0c7547f4ed2d12b148ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301171"
---
# <a name="propertyvalue-property-dao"></a>Свойство Property. Value (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение объекта. Для чтения и записи, **Variant**.

## <a name="syntax"></a>Синтаксис

*Expression* . Оно

*Expression (выражение* ) Переменная, представляющая объект **Property** .

## <a name="remarks"></a>Примечания

Параметр или возвращаемое значение — это тип данных Variant, который оценивается как значение, соответствующее типу данных, как указано в свойстве **Type** объекта.

Как правило, свойство **value** используется для извлечения и изменения данных в объектах **Recordset** .

Свойство **value** является свойством по умолчанию для объектов **field**, **Parameter**и **Property** . Таким образом, вы можете задать или вернуть значение одного из этих объектов, обратившись к ним напрямую вместо того, чтобы указывать свойство **value** .

Попытка задать или вернуть свойство **value** в неприемлемом контексте (например, свойство **value** объекта **field** в коллекции **Fields** объекта **tabledef** ) приведет к ошибке перехвата.

> [!NOTE]
> При чтении десятичных значений из базы данных Microsoft SQL Server они будут отформатированы с использованием экспоненциальной нотации в рабочей области Microsoft Access, но будут отображаться как обычные десятичные значения в рабочей области ODBCDirect.


